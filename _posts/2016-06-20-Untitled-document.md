---
title: FlashPoint
layout: post
author: harry.keyland
permalink: /FlashPoint/
source-id: 1rFD1fSymBDHR0NU8EY2SCA_f7Cu_P7Age_2iwUjZ-Qw
published: true
---
/* When the BBC micro:bit runs  */

function onStart(  ) {

	globals.readyForNewGame = true;

	

}

function onShake(  ) {

	if (globals.readyForNewGame) {

		

		globals.readyForNewGame = false;

		microbit.say(globals.myString);

		microbit.clear();

		wait(Random.number(5000, 10000));

		microbit.draw(Pattern("11111.11111.11111.11111.11111"));

		

	}

	

	

}

function onPressA(  ) {

	if (microbit.isOn(0, 1)) {

		

		microbit.draw(Pattern("00100.01000.11111.01000.00100"));

		

	}

	

	else {

		

		globals.readyForNewGame = true;

		microbit.draw(Pattern("10001.01010.00100.01010.10001"));

		wait(1000);

		microbit.draw(Pattern("00100.00010.11111.00010.00100"));

		globals.readyForNewGame = true;

		

	}

	

	microbit.buttonBPressed;

	if (microbit.isOn(0, 1)) {

		

		microbit.draw(Pattern("00100.00010.11111.00010.00100"));

		else {

			

			microbit.draw(Pattern("10001.01010.00100.01010.10001"));

			wait(1000);

			microbit.draw(Pattern("00100.01000.11111.01000.00100"));

			globals.readyForNewGame = true;

			

