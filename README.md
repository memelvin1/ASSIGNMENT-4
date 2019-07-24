
        [Test]
        public void TheJDPowerInputincorrectcontactnumberExpectedcorrectcontactnumberTest()
        {
            driver.Navigate().GoToUrl("http://localhost/register.html");
            driver.FindElement(By.Name("sellername")).Click();
            driver.FindElement(By.Name("sellername")).Clear();
            driver.FindElement(By.Name("sellername")).SendKeys("john");
            driver.FindElement(By.Name("sellername")).SendKeys(Keys.Down);
            driver.FindElement(By.Name("sellername")).SendKeys(Keys.Down);
            driver.FindElement(By.Name("sellername")).SendKeys(Keys.Tab);
            driver.FindElement(By.Name("address")).Clear();
            driver.FindElement(By.Name("address")).SendKeys("king shoree");
            driver.FindElement(By.Name("city")).Clear();
            driver.FindElement(By.Name("city")).SendKeys("dordan");
            driver.FindElement(By.Name("number")).Clear();
            driver.FindElement(By.Name("number")).SendKeys("1231233455");
            driver.FindElement(By.Name("emailid")).Clear();
            driver.FindElement(By.Name("emailid")).SendKeys("john@gmail.com");
            driver.FindElement(By.Name("vehiclemakee")).Clear();
            driver.FindElement(By.Name("vehiclemakee")).SendKeys("ford");
            driver.FindElement(By.Name("model")).Clear();
            driver.FindElement(By.Name("model")).SendKeys("edge");
            driver.FindElement(By.Name("year")).Clear();
            driver.FindElement(By.Name("year")).SendKeys("2015");
            driver.FindElement(By.Name("sellername")).SendKeys(Keys.Tab);
            driver.FindElement(By.Name("number")).Clear();
            driver.FindElement(By.Name("number")).SendKeys("123-123-3456");
            driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='YEAR:'])[1]/following::input[2]")).Click();
            Assert.AreEqual("http://www.jdpower.com/cars/ford/edge/2015", driver.FindElement(By.LinkText("http://www.jdpower.com/cars/ford/edge/2015")).Text);
        }
        private bool IsElementPresent(By by)
        {
            try
            {
