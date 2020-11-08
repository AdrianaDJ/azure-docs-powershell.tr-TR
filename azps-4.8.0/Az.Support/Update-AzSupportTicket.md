---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/update-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
ms.openlocfilehash: 160d6b4d4a8505c99d5bfcb4c535ec7bbb3b6dd3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267508"
---
# <span data-ttu-id="6da26-101">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="6da26-101">Update-AzSupportTicket</span></span>

## <span data-ttu-id="6da26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6da26-102">SYNOPSIS</span></span>
<span data-ttu-id="6da26-103">Güncelleştirmeler destek bileti.</span><span class="sxs-lookup"><span data-stu-id="6da26-103">Updates support ticket.</span></span>

## <span data-ttu-id="6da26-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6da26-104">SYNTAX</span></span>

### <span data-ttu-id="6da26-105">UpdateByNameWithContactDetailParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6da26-105">UpdateByNameWithContactDetailParameterSet (Default)</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6da26-106">Updatebynamewith, Tobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="6da26-106">UpdateByNameWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] -CustomerContactDetail <PSContactProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6da26-107">UpdateByInputObjectWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="6da26-107">UpdateByInputObjectWithContactDetailParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6da26-108">Updatebyinputobjectwith, Tobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="6da26-108">UpdateByInputObjectWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>]
 -CustomerContactDetail <PSContactProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6da26-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="6da26-109">DESCRIPTION</span></span>
<span data-ttu-id="6da26-110">Destek biletinin önem düzeyini, durumunu veya müşteri iletişim ayrıntılarını güncelleştirmek için bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="6da26-110">Use this cmdlet to update a support ticket's severity level, status or customer contact details.</span></span> <span data-ttu-id="6da26-111">Bilet destek mühendisine atandığında destek biletinin önem düzeyini veya durumunun güncelleştirildiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="6da26-111">Note that updating a support ticket's severity level or status is not allowed when the ticket is assigned to a support engineer.</span></span> <span data-ttu-id="6da26-112">Bilet atamasından sonra önem düzeyini veya durumu güncelleştirmek isterseniz, Bilet üzerinden bir iletişim göndererek destek mühendisine başvurun.</span><span class="sxs-lookup"><span data-stu-id="6da26-112">If you wish to update the severity level or status after ticket assignment, contact the support engineer by sending a communication on the ticket.</span></span>

## <span data-ttu-id="6da26-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6da26-113">EXAMPLES</span></span>

### <span data-ttu-id="6da26-114">Örnek 1: destek biletinin güncelleştirme önem derecesi.</span><span class="sxs-lookup"><span data-stu-id="6da26-114">Example 1: Update severity of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6da26-115">Örnek 2: destek anahtarının güncelleştirme durumu.</span><span class="sxs-lookup"><span data-stu-id="6da26-115">Example 2: Update status of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6da26-116">Örnek 3: kişi nesnesini belirterek destek biletinin iletişim ayrıntılarını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="6da26-116">Example 3: Update contact details of support ticket by specify contact object.</span></span>
```powershell
PS C:\> $contactDetail = new-object Microsoft.Azure.Commands.Support.Models.PSContactProfile
PS C:\> $contactDetail.FirstName = "first name updated"
PS C:\> $contactDetail.LastName = "last name updated"
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerContactDetail $contactDetail 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6da26-117">Örnek 4: destek biletinin destek bileti</span><span class="sxs-lookup"><span data-stu-id="6da26-117">Example 4: Update severity of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6da26-118">Örnek 5: tek tek kişi parametrelerini belirterek destek biletinin iletişim ayrıntılarını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="6da26-118">Example 5: Update contact details of support ticket by specifying individual contact parameters.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerFirstName "first name updated" -CustomerLastName "last name updated" -AdditionalEmailAddress @("user2@contoso.com") 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6da26-119">Örnek 6: destek anahtarının durumunu boru desteği bilet nesnesiyle karşılaştırarak güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="6da26-119">Example 6: Update status of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="6da26-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6da26-120">PARAMETERS</span></span>

### <span data-ttu-id="6da26-121">-Adtionalemapostaadresi</span><span class="sxs-lookup"><span data-stu-id="6da26-121">-AdditionalEmailAddress</span></span>
<span data-ttu-id="6da26-122">Ek e-posta adresleri.</span><span class="sxs-lookup"><span data-stu-id="6da26-122">Additional email addresses.</span></span>
<span data-ttu-id="6da26-123">Burada listelenen e-posta adresleri destek bileti hakkında herhangi bir yazışmadan kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="6da26-123">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da26-124">-Müştercontactdetail</span><span class="sxs-lookup"><span data-stu-id="6da26-124">-CustomerContactDetail</span></span>
<span data-ttu-id="6da26-125">Destek bileti ile Ilgili kişi ayrıntılarını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="6da26-125">Update Contact details on SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: UpdateByNameWithContactObjectParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da26-126">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="6da26-126">-CustomerCountry</span></span>
<span data-ttu-id="6da26-127">Müşteri ülkesi.</span><span class="sxs-lookup"><span data-stu-id="6da26-127">Customer country.</span></span>
<span data-ttu-id="6da26-128">Bu, geçerli bir ISO Alpha-3 ülke kodu (ISO 3166) olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6da26-128">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da26-129">-Müşteradı</span><span class="sxs-lookup"><span data-stu-id="6da26-129">-CustomerFirstName</span></span>
<span data-ttu-id="6da26-130">Müşteri adı.</span><span class="sxs-lookup"><span data-stu-id="6da26-130">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da26-131">-Müşterlastname</span><span class="sxs-lookup"><span data-stu-id="6da26-131">-CustomerLastName</span></span>
<span data-ttu-id="6da26-132">Müşterinin soyadı.</span><span class="sxs-lookup"><span data-stu-id="6da26-132">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da26-133">-Müştertelefonnumarası</span><span class="sxs-lookup"><span data-stu-id="6da26-133">-CustomerPhoneNumber</span></span>
<span data-ttu-id="6da26-134">Müşteri telefon numarası.</span><span class="sxs-lookup"><span data-stu-id="6da26-134">Customer phone number.</span></span>
<span data-ttu-id="6da26-135">Tercih edilen kişi yöntemi telefon ise bu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6da26-135">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da26-136">-Müşterpreferredsupportsupport</span><span class="sxs-lookup"><span data-stu-id="6da26-136">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="6da26-137">Müşteri tarafından tercih edilen destek dili.</span><span class="sxs-lookup"><span data-stu-id="6da26-137">Customer preferred support language.</span></span>
<span data-ttu-id="6da26-138">Burada listelenen desteklenen dillerden birinin geçerli bir dil-Contry kodu olması gerekir https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="6da26-138">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da26-139">-Müşterpreferredtimezone</span><span class="sxs-lookup"><span data-stu-id="6da26-139">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="6da26-140">Müşterinin tercih ettiği saat dilimi.</span><span class="sxs-lookup"><span data-stu-id="6da26-140">Customer preferred time zone.</span></span>
<span data-ttu-id="6da26-141">Bu geçerli bir System.TimeZoneInfo.Id değeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6da26-141">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da26-142">-Müştergunlubir Yemapostaadresi</span><span class="sxs-lookup"><span data-stu-id="6da26-142">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="6da26-143">Müşteri birincil e-posta adresi.</span><span class="sxs-lookup"><span data-stu-id="6da26-143">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da26-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6da26-144">-DefaultProfile</span></span>
<span data-ttu-id="6da26-145">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6da26-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da26-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6da26-146">-InputObject</span></span>
<span data-ttu-id="6da26-147">Bu cmdlet 'in güncelleştirdiği SupportTicket kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6da26-147">SupportTicket resource object that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: UpdateByInputObjectWithContactDetailParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6da26-148">-Ad</span><span class="sxs-lookup"><span data-stu-id="6da26-148">-Name</span></span>
<span data-ttu-id="6da26-149">Bu cmdlet 'in güncelleştirdiği SupportTicket kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="6da26-149">Name of SupportTicket resource that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByNameWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da26-150">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="6da26-150">-PreferredContactMethod</span></span>
<span data-ttu-id="6da26-151">Tercih edilen kişi yöntemi.</span><span class="sxs-lookup"><span data-stu-id="6da26-151">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da26-152">-Önem derecesi</span><span class="sxs-lookup"><span data-stu-id="6da26-152">-Severity</span></span>
<span data-ttu-id="6da26-153">Destek anahtarının önem derecesi.</span><span class="sxs-lookup"><span data-stu-id="6da26-153">Update Severity of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da26-154">-Durum</span><span class="sxs-lookup"><span data-stu-id="6da26-154">-Status</span></span>
<span data-ttu-id="6da26-155">Destek anahtarının güncelleştirme durumu.</span><span class="sxs-lookup"><span data-stu-id="6da26-155">Update Status of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Status
Parameter Sets: (All)
Aliases:
Accepted values: Open, Closed

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da26-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="6da26-156">-Confirm</span></span>
<span data-ttu-id="6da26-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6da26-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da26-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6da26-158">-WhatIf</span></span>
<span data-ttu-id="6da26-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6da26-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6da26-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6da26-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6da26-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da26-161">CommonParameters</span></span>
<span data-ttu-id="6da26-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6da26-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da26-163">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6da26-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da26-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6da26-164">INPUTS</span></span>

### <span data-ttu-id="6da26-165">Microsoft. Azure. Commands. support. model. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="6da26-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="6da26-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6da26-166">OUTPUTS</span></span>

### <span data-ttu-id="6da26-167">Microsoft. Azure. Commands. support. model. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="6da26-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="6da26-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6da26-168">NOTES</span></span>

## <span data-ttu-id="6da26-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6da26-169">RELATED LINKS</span></span>
