## Mellt

Fe awn ati i alluogi'r llong ofod saethu mellt!

+ Ychwanega'r ciplun 'Mellt' o'r llyfrgell Scratch.  Pan mae'r gêm yn cychwyn, fe ddylai'r mellt fod yn guddiedig tan bod y llong ofod yn tanio ei laser. Bydd angen i'r ciplun fod yn fach a ben ei waered. Ychwanega'r côd canlynol i'r ciplun Mellt.

	```blocks
		pan fo ⚑ wedi ei glicio
			cuddio
			gosod maint i (25)%
		pwyntio i gyfeiriad (-90 v)
	```


+ Ychwanega'r côd canlynol **i'r Llong ofod** i greu mellten newydd pryd bynnag mae'r bylchwr yn cael ei wasgu.


	```blocks
		pan fo ⚑ wedi ei glicio
			am byth
   		os <bysell [bylchwr v] wedi ei wasgu?> wedyn
      		creu clôn o [Lightning v]
   			end
		end
	```

+ Pryd bynnag mae 'na glôn newydd yn cael ei greu, fe ddylai gychwyn yn yr un lle â'r llong ofod, ac yna symud fyny'r llwyfan tan ei fod yn cyffwrdd yr ochr. Ychwanega'r côd yma i giplun y **Mellt**:

	```blocks
		pan dechreuaf fel clôn
			mynd i [Spaceship v]
			dangos
		ailwna hyd at <cyffwrdd [ymyl v]?>
   			newid y gan (10)
		end
			dileu y clôn hwn
	```

Nodyn: Rydyn ni'n symud y clôn newydd i'r llong ofod tra mae dal wedi cuddio, cyn ei ddangos. Mae'n edrych yn neisach!

+ Profa dy fellt trwy wasgu'r bylchwr.


--- challenge ---
### Her: Trwsio'r fellten
Beth sy'n digwydd os wyt ti'n cadw gwasgu ar y bylchwr? Wyt ti'n gallu defnyddio bloc 'aros' {.blockcontrol} i ddatrys hyn?

--- /challenge ---
