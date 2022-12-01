import pytest
from main import check_psw
from main import check_email
from main import check_psw_equal
from main import check_credentials

#Tests to question 1: -------------------------------
def test_email1():
  email = "myname326@gmail.com"
  assert check_email(email) is True

def test_email2():
  email = "my.ownsite@acn.org"
  assert check_email(email) is True

def test_email3():
  email = "myname326.com"
  assert check_email(email) is False

def test_check_psw1():
  psw = "Qwert1234"
  assert check_psw(psw) is True

def test_check_psw2():
  psw = "qwert"
  assert check_psw(psw) is False

def test_check_psw3():
  psw = "QWERT55"
  assert check_psw(psw) is False
  
def test_check_psw4():
  psw = "Qwerty"
  assert check_psw(psw) is False
  
def test_check_psw5():
  psw = "551234"
  assert check_psw(psw) is False

def test_check_psw6():
  psw = "Qwerty$Â£@55"
  assert check_psw(psw) is True

def test_check_psw7():
  psw = "Qwerty$Â£@"
  assert check_psw(psw) is False

def test_check_psw8():
  psw = "Qwert5@"
  assert check_psw(psw) is False     

# TODO write the unit tests for the new functions, replace pass with your code: ---------------------------- 
#1. Test that two equal passwords return true
def test_psw_equal1():
  psw1 = "Abcd1234"
  psw2 = "Abcd1234"
  assert check_psw_equal(psw1, psw2) is True


#2. Test that the function is not case sencative
def test_psw_equal2():
  psw1 = "aBCD1234"
  psw2 = "Abcd1234"
  assert check_psw_equal(psw1, psw2) is False

# 3. Test that two inequal passwords return false
def test_psw_equal3():
  psw1 = "Abcd1234"
  psw2 = "Efgh5678"
  assert check_psw_equal(psw1, psw2) is False

# 4. Test that two equal passwords in the correct format and a correct email return true
def test_check_credentials1():
  psw1 = "Abcd1234"
  psw2 = "Abcd1234"
  email = "acnnordics@acnnordics.com"
  assert check_credentials(email, psw1, psw2) is True

#5. Test that two inequal passwords in the correct format and a correct email return false
def test_check_credentials2():
  psw1 = "Abcd1234"
  psw2 = "Efgh5678"
  email = "acnnordics@acnnordics.com"
  assert check_credentials(email, psw1, psw2) is False

# 6. Test that two equal passwords in the correct format and an incorrect email return false
def test_check_credentials3():
  psw1 = "Abcd1234"
  psw2 = "Abcd1234"
  email = "@acnnordics.com"
  assert check_credentials(email, psw1, psw2) is False
