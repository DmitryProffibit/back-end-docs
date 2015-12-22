!!!!Тут есть и стандартные круд и методы!!!!!
----------------


GET subject/waitForVerify
----------------
RESPONCE:
	[
		{
			...companyFields OR ...profileFields
		},
	]

	Возвращает сабжекты ожидающие верификации


PUT subject/setVerify/:subjectId
----------------
DATA:
  { verifyState: 1|2|3|4 }

    Установить состояние верификации verifyState одно из

	verifyStates:{
	  NEW: 0,
	  TO_VERIFY: 1,
	  DONE: 2,
	  REJECTED: 3
	}