GET public/company/
----------------
RESPONCE:
	[
		{
			...companyFields, roles:{...roleFields}
		},
	]

	Возвращает перечень компаний к которым относится (работает там) текущий пользователь.


GET public/company/:subjectId
----------------
RESPONCE:
	{
		...companyFields, employees:{...profileFields}
	}

	Возвращает компанию с сотрудниками


POST public/company
----------------
DATA:
    {
	    "subjectType":1,
	    "lastName":"sample lastName",
	    "passSeria":"sample passSeria",
	    "passNum":"42",
	    "passIssuedBy":"sample passIssuedBy",
	    "passDate":"Wed Dec 16 2015 10:42:46 GMT+0200 (EET)",
	    "bankIdent":"sample bankIdent",
	    "bankName":"sample bankName"
    }
RESPONCE:
	{ ...companyFields}

	Добавит новую компанию 
	

PUT public/company/:subjectId
----------------
RESPONCE:
    {
	    "lastName":"sample lastName",
	    "passSeria":"sample passSeria",
    }

	Обновит компанию :subjectId 


POST public/company/addEmployee
----------------
DATA:
    {
	    subjectId,
	    emails: ["email1", "email2"]
    }
RESPONCE:
	[ { ...profileFields, role: { ...roleFields } } ]

	Добавит профили с почтой указаной в emails в сотрудников компании subjectId. Вернёт масив добавленых пользователей. Добавленых ранее или ненайденных - не вернёт.
