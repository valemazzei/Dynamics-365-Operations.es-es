## <a name="customers-v3-to-accounts"></a><span data-ttu-id="ddec3-101">Clientes V3 para cuentas</span><span class="sxs-lookup"><span data-stu-id="ddec3-101">Customers V3 to accounts</span></span>

<span data-ttu-id="ddec3-102">Esta plantilla sincroniza datos entre aplicaciones de Finance and Operations y Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ddec3-102">This template synchronizes data between Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="ddec3-103">Filtro de origen: ((PartyType == "Organización"))</span><span class="sxs-lookup"><span data-stu-id="ddec3-103">Source filter: ((PartyType == "Organization"))</span></span>

<span data-ttu-id="ddec3-104">Filtro de origen invertido: customertypecode eq 3</span><span class="sxs-lookup"><span data-stu-id="ddec3-104">Reversed source filter: customertypecode eq 3</span></span>

<span data-ttu-id="ddec3-105">Campo de Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ddec3-105">Finance and Operations field</span></span> | <span data-ttu-id="ddec3-106">Tipo de asignación</span><span class="sxs-lookup"><span data-stu-id="ddec3-106">Map type</span></span> | <span data-ttu-id="ddec3-107">Otro campo de Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ddec3-107">Other Dynamics 365 field</span></span> | <span data-ttu-id="ddec3-108">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="ddec3-108">Default value</span></span>
---|---|---|---
<span data-ttu-id="ddec3-109">CUSTOMERACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ddec3-109">CUSTOMERACCOUNT</span></span> | = | <span data-ttu-id="ddec3-110">accountnumber</span><span class="sxs-lookup"><span data-stu-id="ddec3-110">accountnumber</span></span> | 
<span data-ttu-id="ddec3-111">INVOICEADDRESSCITY</span><span class="sxs-lookup"><span data-stu-id="ddec3-111">INVOICEADDRESSCITY</span></span> | = | <span data-ttu-id="ddec3-112">address2_city</span><span class="sxs-lookup"><span data-stu-id="ddec3-112">address2_city</span></span> | 
<span data-ttu-id="ddec3-113">INVOICEADDRESSCOUNTRYREGIONISOCODE</span><span class="sxs-lookup"><span data-stu-id="ddec3-113">INVOICEADDRESSCOUNTRYREGIONISOCODE</span></span> | = | <span data-ttu-id="ddec3-114">address2_country</span><span class="sxs-lookup"><span data-stu-id="ddec3-114">address2_country</span></span> | 
<span data-ttu-id="ddec3-115">INVOICEADDRESSCOUNTY</span><span class="sxs-lookup"><span data-stu-id="ddec3-115">INVOICEADDRESSCOUNTY</span></span> | = | <span data-ttu-id="ddec3-116">address2_county</span><span class="sxs-lookup"><span data-stu-id="ddec3-116">address2_county</span></span> | 
<span data-ttu-id="ddec3-117">INVOICEADDRESSLATITUDE</span><span class="sxs-lookup"><span data-stu-id="ddec3-117">INVOICEADDRESSLATITUDE</span></span> | > | <span data-ttu-id="ddec3-118">address2_latitude</span><span class="sxs-lookup"><span data-stu-id="ddec3-118">address2_latitude</span></span> | 
<span data-ttu-id="ddec3-119">INVOICEADDRESSLONGITUDE</span><span class="sxs-lookup"><span data-stu-id="ddec3-119">INVOICEADDRESSLONGITUDE</span></span> | > | <span data-ttu-id="ddec3-120">address2_longitude</span><span class="sxs-lookup"><span data-stu-id="ddec3-120">address2_longitude</span></span> | 
<span data-ttu-id="ddec3-121">INVOICEADDRESSSTATE</span><span class="sxs-lookup"><span data-stu-id="ddec3-121">INVOICEADDRESSSTATE</span></span> | = | <span data-ttu-id="ddec3-122">address2_stateorprovince</span><span class="sxs-lookup"><span data-stu-id="ddec3-122">address2_stateorprovince</span></span> | 
<span data-ttu-id="ddec3-123">INVOICEADDRESSSTREET</span><span class="sxs-lookup"><span data-stu-id="ddec3-123">INVOICEADDRESSSTREET</span></span> | = | <span data-ttu-id="ddec3-124">address2_line1</span><span class="sxs-lookup"><span data-stu-id="ddec3-124">address2_line1</span></span> | 
<span data-ttu-id="ddec3-125">INVOICEADDRESSZIPCODE</span><span class="sxs-lookup"><span data-stu-id="ddec3-125">INVOICEADDRESSZIPCODE</span></span> | = | <span data-ttu-id="ddec3-126">address2_postalcode</span><span class="sxs-lookup"><span data-stu-id="ddec3-126">address2_postalcode</span></span> | 
<span data-ttu-id="ddec3-127">CREDITLIMIT</span><span class="sxs-lookup"><span data-stu-id="ddec3-127">CREDITLIMIT</span></span> | = | <span data-ttu-id="ddec3-128">creditlimit</span><span class="sxs-lookup"><span data-stu-id="ddec3-128">creditlimit</span></span> | 
<span data-ttu-id="ddec3-129">DELIVERYADDRESSCITY</span><span class="sxs-lookup"><span data-stu-id="ddec3-129">DELIVERYADDRESSCITY</span></span> | = | <span data-ttu-id="ddec3-130">address1_city</span><span class="sxs-lookup"><span data-stu-id="ddec3-130">address1_city</span></span> | 
<span data-ttu-id="ddec3-131">DELIVERYADDRESSCOUNTRYREGIONISOCODE</span><span class="sxs-lookup"><span data-stu-id="ddec3-131">DELIVERYADDRESSCOUNTRYREGIONISOCODE</span></span> | = | <span data-ttu-id="ddec3-132">address1_country</span><span class="sxs-lookup"><span data-stu-id="ddec3-132">address1_country</span></span> | 
<span data-ttu-id="ddec3-133">DELIVERYADDRESSCOUNTY</span><span class="sxs-lookup"><span data-stu-id="ddec3-133">DELIVERYADDRESSCOUNTY</span></span> | = | <span data-ttu-id="ddec3-134">address1_county</span><span class="sxs-lookup"><span data-stu-id="ddec3-134">address1_county</span></span> | 
<span data-ttu-id="ddec3-135">DELIVERYADDRESSLATITUDE</span><span class="sxs-lookup"><span data-stu-id="ddec3-135">DELIVERYADDRESSLATITUDE</span></span> | > | <span data-ttu-id="ddec3-136">address1_latitude</span><span class="sxs-lookup"><span data-stu-id="ddec3-136">address1_latitude</span></span> | 
<span data-ttu-id="ddec3-137">DELIVERYADDRESSLONGITUDE</span><span class="sxs-lookup"><span data-stu-id="ddec3-137">DELIVERYADDRESSLONGITUDE</span></span> | > | <span data-ttu-id="ddec3-138">address1_longitude</span><span class="sxs-lookup"><span data-stu-id="ddec3-138">address1_longitude</span></span> | 
<span data-ttu-id="ddec3-139">DELIVERYADDRESSZIPCODE</span><span class="sxs-lookup"><span data-stu-id="ddec3-139">DELIVERYADDRESSZIPCODE</span></span> | = | <span data-ttu-id="ddec3-140">address1_postalcode</span><span class="sxs-lookup"><span data-stu-id="ddec3-140">address1_postalcode</span></span> | 
<span data-ttu-id="ddec3-141">ORGANIZATIONNAME</span><span class="sxs-lookup"><span data-stu-id="ddec3-141">ORGANIZATIONNAME</span></span> | = | <span data-ttu-id="ddec3-142">name</span><span class="sxs-lookup"><span data-stu-id="ddec3-142">name</span></span> | 
<span data-ttu-id="ddec3-143">ORGANIZATIONNUMBEROFEMPLOYEES</span><span class="sxs-lookup"><span data-stu-id="ddec3-143">ORGANIZATIONNUMBEROFEMPLOYEES</span></span> | = | <span data-ttu-id="ddec3-144">numberofemployees</span><span class="sxs-lookup"><span data-stu-id="ddec3-144">numberofemployees</span></span> | 
<span data-ttu-id="ddec3-145">PRIMARYCONTACTEMAIL</span><span class="sxs-lookup"><span data-stu-id="ddec3-145">PRIMARYCONTACTEMAIL</span></span> | = | <span data-ttu-id="ddec3-146">emailaddress1</span><span class="sxs-lookup"><span data-stu-id="ddec3-146">emailaddress1</span></span> | 
<span data-ttu-id="ddec3-147">PRIMARYCONTACTFAX</span><span class="sxs-lookup"><span data-stu-id="ddec3-147">PRIMARYCONTACTFAX</span></span> | = | <span data-ttu-id="ddec3-148">fax</span><span class="sxs-lookup"><span data-stu-id="ddec3-148">fax</span></span> | 
<span data-ttu-id="ddec3-149">PRIMARYCONTACTPHONE</span><span class="sxs-lookup"><span data-stu-id="ddec3-149">PRIMARYCONTACTPHONE</span></span> | = | <span data-ttu-id="ddec3-150">telephone1</span><span class="sxs-lookup"><span data-stu-id="ddec3-150">telephone1</span></span> | 
<span data-ttu-id="ddec3-151">PRIMARYCONTACTTWITTER</span><span class="sxs-lookup"><span data-stu-id="ddec3-151">PRIMARYCONTACTTWITTER</span></span> | = | <span data-ttu-id="ddec3-152">primarytwitterid</span><span class="sxs-lookup"><span data-stu-id="ddec3-152">primarytwitterid</span></span> | 
<span data-ttu-id="ddec3-153">PRIMARYCONTACTURL</span><span class="sxs-lookup"><span data-stu-id="ddec3-153">PRIMARYCONTACTURL</span></span> | = | <span data-ttu-id="ddec3-154">websiteurl</span><span class="sxs-lookup"><span data-stu-id="ddec3-154">websiteurl</span></span> | 
<span data-ttu-id="ddec3-155">SALESCURRENCYCODE</span><span class="sxs-lookup"><span data-stu-id="ddec3-155">SALESCURRENCYCODE</span></span> | = | <span data-ttu-id="ddec3-156">transactioncurrencyid.isocurrencycode</span><span class="sxs-lookup"><span data-stu-id="ddec3-156">transactioncurrencyid.isocurrencycode</span></span> | 
<span data-ttu-id="ddec3-157">SALESMEMO</span><span class="sxs-lookup"><span data-stu-id="ddec3-157">SALESMEMO</span></span> | = | <span data-ttu-id="ddec3-158">descripción</span><span class="sxs-lookup"><span data-stu-id="ddec3-158">description</span></span> | 
<span data-ttu-id="ddec3-159">CREDITLIMITISMANDATORY</span><span class="sxs-lookup"><span data-stu-id="ddec3-159">CREDITLIMITISMANDATORY</span></span> | >< | <span data-ttu-id="ddec3-160">msdyn_creditlimitismandatory</span><span class="sxs-lookup"><span data-stu-id="ddec3-160">msdyn_creditlimitismandatory</span></span> | 
<span data-ttu-id="ddec3-161">CREDITRATING</span><span class="sxs-lookup"><span data-stu-id="ddec3-161">CREDITRATING</span></span> | = | <span data-ttu-id="ddec3-162">msdyn_creditrating</span><span class="sxs-lookup"><span data-stu-id="ddec3-162">msdyn_creditrating</span></span> | 
<span data-ttu-id="ddec3-163">CUSTOMERGROUPID</span><span class="sxs-lookup"><span data-stu-id="ddec3-163">CUSTOMERGROUPID</span></span> | = | <span data-ttu-id="ddec3-164">msdyn_customergroupid.msdyn_groupid</span><span class="sxs-lookup"><span data-stu-id="ddec3-164">msdyn_customergroupid.msdyn_groupid</span></span> | 
<span data-ttu-id="ddec3-165">IDENTIFICATIONNUMBER</span><span class="sxs-lookup"><span data-stu-id="ddec3-165">IDENTIFICATIONNUMBER</span></span> | = | <span data-ttu-id="ddec3-166">msdyn_identificationnumber</span><span class="sxs-lookup"><span data-stu-id="ddec3-166">msdyn_identificationnumber</span></span> | 
<span data-ttu-id="ddec3-167">INVOICEACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ddec3-167">INVOICEACCOUNT</span></span> | = | <span data-ttu-id="ddec3-168">msdyn_billingaccount.accountnumber</span><span class="sxs-lookup"><span data-stu-id="ddec3-168">msdyn_billingaccount.accountnumber</span></span> | 
<span data-ttu-id="ddec3-169">INVOICEADDRESS</span><span class="sxs-lookup"><span data-stu-id="ddec3-169">INVOICEADDRESS</span></span> | >< | <span data-ttu-id="ddec3-170">msdyn_invoiceaddress</span><span class="sxs-lookup"><span data-stu-id="ddec3-170">msdyn_invoiceaddress</span></span> | 
<span data-ttu-id="ddec3-171">ISONETIMECUSTOMER</span><span class="sxs-lookup"><span data-stu-id="ddec3-171">ISONETIMECUSTOMER</span></span> | >< | <span data-ttu-id="ddec3-172">msdyn_onetimecustomer</span><span class="sxs-lookup"><span data-stu-id="ddec3-172">msdyn_onetimecustomer</span></span> | 
<span data-ttu-id="ddec3-173">ONHOLDSTATUS</span><span class="sxs-lookup"><span data-stu-id="ddec3-173">ONHOLDSTATUS</span></span> | >< | <span data-ttu-id="ddec3-174">msdyn_onholdstatus</span><span class="sxs-lookup"><span data-stu-id="ddec3-174">msdyn_onholdstatus</span></span> | 
<span data-ttu-id="ddec3-175">PARTYCOUNTRY</span><span class="sxs-lookup"><span data-stu-id="ddec3-175">PARTYCOUNTRY</span></span> | = | <span data-ttu-id="ddec3-176">msdyn_partycountry</span><span class="sxs-lookup"><span data-stu-id="ddec3-176">msdyn_partycountry</span></span> | 
<span data-ttu-id="ddec3-177">PARTYSTATE</span><span class="sxs-lookup"><span data-stu-id="ddec3-177">PARTYSTATE</span></span> | = | <span data-ttu-id="ddec3-178">msdyn_partystateprovince</span><span class="sxs-lookup"><span data-stu-id="ddec3-178">msdyn_partystateprovince</span></span> | 
<span data-ttu-id="ddec3-179">PAYMENTDAY</span><span class="sxs-lookup"><span data-stu-id="ddec3-179">PAYMENTDAY</span></span> | = | <span data-ttu-id="ddec3-180">msdyn_paymentday.msdyn_name</span><span class="sxs-lookup"><span data-stu-id="ddec3-180">msdyn_paymentday.msdyn_name</span></span> | 
<span data-ttu-id="ddec3-181">PAYMENTMETHOD</span><span class="sxs-lookup"><span data-stu-id="ddec3-181">PAYMENTMETHOD</span></span> | = | <span data-ttu-id="ddec3-182">msdyn_customerpaymentmethod.msdyn_name</span><span class="sxs-lookup"><span data-stu-id="ddec3-182">msdyn_customerpaymentmethod.msdyn_name</span></span> | 
<span data-ttu-id="ddec3-183">PAYMENTSCHEDULE</span><span class="sxs-lookup"><span data-stu-id="ddec3-183">PAYMENTSCHEDULE</span></span> | = | <span data-ttu-id="ddec3-184">msdyn_paymentschedule.msdyn_name</span><span class="sxs-lookup"><span data-stu-id="ddec3-184">msdyn_paymentschedule.msdyn_name</span></span> | 
<span data-ttu-id="ddec3-185">PAYMENTTERMS</span><span class="sxs-lookup"><span data-stu-id="ddec3-185">PAYMENTTERMS</span></span> | = | <span data-ttu-id="ddec3-186">msdyn_paymentterm.msdyn_name</span><span class="sxs-lookup"><span data-stu-id="ddec3-186">msdyn_paymentterm.msdyn_name</span></span> | 
<span data-ttu-id="ddec3-187">PAYMENTTERMSBASEDAYS</span><span class="sxs-lookup"><span data-stu-id="ddec3-187">PAYMENTTERMSBASEDAYS</span></span> | = | <span data-ttu-id="ddec3-188">msdyn_paymenttermsbasedays</span><span class="sxs-lookup"><span data-stu-id="ddec3-188">msdyn_paymenttermsbasedays</span></span> | 
<span data-ttu-id="ddec3-189">PRIMARYCONTACTFACEBOOK</span><span class="sxs-lookup"><span data-stu-id="ddec3-189">PRIMARYCONTACTFACEBOOK</span></span> | = | <span data-ttu-id="ddec3-190">msdyn_primaryfacebookid</span><span class="sxs-lookup"><span data-stu-id="ddec3-190">msdyn_primaryfacebookid</span></span> | 
<span data-ttu-id="ddec3-191">PRIMARYCONTACTFAXEXTENSION</span><span class="sxs-lookup"><span data-stu-id="ddec3-191">PRIMARYCONTACTFAXEXTENSION</span></span> | = | <span data-ttu-id="ddec3-192">msdyn_faxextension</span><span class="sxs-lookup"><span data-stu-id="ddec3-192">msdyn_faxextension</span></span> | 
<span data-ttu-id="ddec3-193">PRIMARYCONTACTLINKEDIN</span><span class="sxs-lookup"><span data-stu-id="ddec3-193">PRIMARYCONTACTLINKEDIN</span></span> | = | <span data-ttu-id="ddec3-194">msdyn_primarylinkedinid</span><span class="sxs-lookup"><span data-stu-id="ddec3-194">msdyn_primarylinkedinid</span></span> | 
<span data-ttu-id="ddec3-195">TAXEXEMPTNUMBER</span><span class="sxs-lookup"><span data-stu-id="ddec3-195">TAXEXEMPTNUMBER</span></span> | = | <span data-ttu-id="ddec3-196">msdyn_taxexemptnumber</span><span class="sxs-lookup"><span data-stu-id="ddec3-196">msdyn_taxexemptnumber</span></span> | 
<span data-ttu-id="ddec3-197">VENDORACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ddec3-197">VENDORACCOUNT</span></span> | = | <span data-ttu-id="ddec3-198">msdyn_vendor.msdyn_vendoraccountnumber</span><span class="sxs-lookup"><span data-stu-id="ddec3-198">msdyn_vendor.msdyn_vendoraccountnumber</span></span> | 
<span data-ttu-id="ddec3-199">PRIMARYCONTACTEMAILDESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ddec3-199">PRIMARYCONTACTEMAILDESCRIPTION</span></span> | = | <span data-ttu-id="ddec3-200">msdyn_emailaddress1description</span><span class="sxs-lookup"><span data-stu-id="ddec3-200">msdyn_emailaddress1description</span></span> | 
<span data-ttu-id="ddec3-201">PRIMARYCONTACTFACEBOOKDESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ddec3-201">PRIMARYCONTACTFACEBOOKDESCRIPTION</span></span> | = | <span data-ttu-id="ddec3-202">msdyn_primaryfacebookdescription</span><span class="sxs-lookup"><span data-stu-id="ddec3-202">msdyn_primaryfacebookdescription</span></span> | 
<span data-ttu-id="ddec3-203">PRIMARYCONTACTFAXDESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ddec3-203">PRIMARYCONTACTFAXDESCRIPTION</span></span> | = | <span data-ttu-id="ddec3-204">msdyn_faxdescription</span><span class="sxs-lookup"><span data-stu-id="ddec3-204">msdyn_faxdescription</span></span> | 
<span data-ttu-id="ddec3-205">PRIMARYCONTACTLINKEDINDESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ddec3-205">PRIMARYCONTACTLINKEDINDESCRIPTION</span></span> | = | <span data-ttu-id="ddec3-206">msdyn_primarylinkedindescrption</span><span class="sxs-lookup"><span data-stu-id="ddec3-206">msdyn_primarylinkedindescrption</span></span> | 
<span data-ttu-id="ddec3-207">PRIMARYCONTACTPHONEDESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ddec3-207">PRIMARYCONTACTPHONEDESCRIPTION</span></span> | = | <span data-ttu-id="ddec3-208">msdyn_telephone1description</span><span class="sxs-lookup"><span data-stu-id="ddec3-208">msdyn_telephone1description</span></span> | 
<span data-ttu-id="ddec3-209">PRIMARYCONTACTPHONEEXTENSION</span><span class="sxs-lookup"><span data-stu-id="ddec3-209">PRIMARYCONTACTPHONEEXTENSION</span></span> | = | <span data-ttu-id="ddec3-210">msdyn_telephone1extension</span><span class="sxs-lookup"><span data-stu-id="ddec3-210">msdyn_telephone1extension</span></span> | 
<span data-ttu-id="ddec3-211">PRIMARYCONTACTTWITTERDESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ddec3-211">PRIMARYCONTACTTWITTERDESCRIPTION</span></span> | = | <span data-ttu-id="ddec3-212">msdyn_primarytwitteriddescription</span><span class="sxs-lookup"><span data-stu-id="ddec3-212">msdyn_primarytwitteriddescription</span></span> | 
<span data-ttu-id="ddec3-213">PRIMARYCONTACTURLDESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ddec3-213">PRIMARYCONTACTURLDESCRIPTION</span></span> | = | <span data-ttu-id="ddec3-214">msdyn_websiteurldescription</span><span class="sxs-lookup"><span data-stu-id="ddec3-214">msdyn_websiteurldescription</span></span> | 
<span data-ttu-id="ddec3-215">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="ddec3-215">LANGUAGEID</span></span> | << | <span data-ttu-id="ddec3-216">none</span><span class="sxs-lookup"><span data-stu-id="ddec3-216">none</span></span> | <span data-ttu-id="ddec3-217">es</span><span class="sxs-lookup"><span data-stu-id="ddec3-217">en-us</span></span>
<span data-ttu-id="ddec3-218">DELIVERYADDRESSSTREET</span><span class="sxs-lookup"><span data-stu-id="ddec3-218">DELIVERYADDRESSSTREET</span></span> | = | <span data-ttu-id="ddec3-219">address1_line1</span><span class="sxs-lookup"><span data-stu-id="ddec3-219">address1_line1</span></span> | 
<span data-ttu-id="ddec3-220">DELIVERYADDRESSSTATE</span><span class="sxs-lookup"><span data-stu-id="ddec3-220">DELIVERYADDRESSSTATE</span></span> | = | <span data-ttu-id="ddec3-221">address1_stateorprovince</span><span class="sxs-lookup"><span data-stu-id="ddec3-221">address1_stateorprovince</span></span> | 
<span data-ttu-id="ddec3-222">none</span><span class="sxs-lookup"><span data-stu-id="ddec3-222">none</span></span> | >> | <span data-ttu-id="ddec3-223">address1_addresstypecode</span><span class="sxs-lookup"><span data-stu-id="ddec3-223">address1_addresstypecode</span></span> | <span data-ttu-id="ddec3-224">2</span><span class="sxs-lookup"><span data-stu-id="ddec3-224">2</span></span>
<span data-ttu-id="ddec3-225">none</span><span class="sxs-lookup"><span data-stu-id="ddec3-225">none</span></span> | >> | <span data-ttu-id="ddec3-226">customertypecode</span><span class="sxs-lookup"><span data-stu-id="ddec3-226">customertypecode</span></span> | <span data-ttu-id="ddec3-227">3</span><span class="sxs-lookup"><span data-stu-id="ddec3-227">3</span></span>
<span data-ttu-id="ddec3-228">PARTYTYPE</span><span class="sxs-lookup"><span data-stu-id="ddec3-228">PARTYTYPE</span></span> | << | <span data-ttu-id="ddec3-229">none</span><span class="sxs-lookup"><span data-stu-id="ddec3-229">none</span></span> | <span data-ttu-id="ddec3-230">Organización</span><span class="sxs-lookup"><span data-stu-id="ddec3-230">Organization</span></span>
<span data-ttu-id="ddec3-231">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="ddec3-231">PARTYNUMBER</span></span> | = | <span data-ttu-id="ddec3-232">msdyn_partynumber</span><span class="sxs-lookup"><span data-stu-id="ddec3-232">msdyn_partynumber</span></span> | 
<span data-ttu-id="ddec3-233">CONTACTPERSONID</span><span class="sxs-lookup"><span data-stu-id="ddec3-233">CONTACTPERSONID</span></span> | = | <span data-ttu-id="ddec3-234">primarycontactid.msdyn_contactpersonid</span><span class="sxs-lookup"><span data-stu-id="ddec3-234">primarycontactid.msdyn_contactpersonid</span></span> | 