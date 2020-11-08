---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268647"
---
# <span data-ttu-id="a2e45-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="a2e45-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="a2e45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2e45-102">SYNOPSIS</span></span>
<span data-ttu-id="a2e45-103">Destek kişi profili nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a2e45-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="a2e45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2e45-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2e45-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2e45-105">DESCRIPTION</span></span>
<span data-ttu-id="a2e45-106">Bu, destek bileti oluştururken veya güncelleştirirken bir destek kişi profili nesnesi oluşturmak için kullanabileceğiniz bir yardımcı cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2e45-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="a2e45-107">Destek bileti oluşturmak için zorunlu olan aşağıdaki parametreleri belirtmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="a2e45-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="a2e45-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2e45-108">EXAMPLES</span></span>

### <span data-ttu-id="a2e45-109">Örnek 1: kişi nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a2e45-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="a2e45-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2e45-110">PARAMETERS</span></span>

### <span data-ttu-id="a2e45-111">-Adtionalemapostaadresi</span><span class="sxs-lookup"><span data-stu-id="a2e45-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="a2e45-112">Burada listelenen e-posta adresleri destek bileti hakkında herhangi bir yazışmadan kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="a2e45-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e45-113">-Ülke</span><span class="sxs-lookup"><span data-stu-id="a2e45-113">-Country</span></span>
<span data-ttu-id="a2e45-114">Müşteri ülkesi.</span><span class="sxs-lookup"><span data-stu-id="a2e45-114">Customer country.</span></span>
<span data-ttu-id="a2e45-115">Bu, geçerli bir ISO Alpha-3 ülke kodu (ISO 3166) olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a2e45-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e45-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2e45-116">-DefaultProfile</span></span>
<span data-ttu-id="a2e45-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a2e45-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2e45-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="a2e45-118">-FirstName</span></span>
<span data-ttu-id="a2e45-119">Müşteri adı.</span><span class="sxs-lookup"><span data-stu-id="a2e45-119">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e45-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="a2e45-120">-LastName</span></span>
<span data-ttu-id="a2e45-121">Müşterinin soyadı.</span><span class="sxs-lookup"><span data-stu-id="a2e45-121">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e45-122">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="a2e45-122">-PhoneNumber</span></span>
<span data-ttu-id="a2e45-123">Müşteri telefon numarası.</span><span class="sxs-lookup"><span data-stu-id="a2e45-123">Customer phone number.</span></span>
<span data-ttu-id="a2e45-124">Tercih edilen kişi yöntemi telefon ise bu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a2e45-124">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e45-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="a2e45-125">-PreferredContactMethod</span></span>
<span data-ttu-id="a2e45-126">Tercih edilen kişi yöntemi.</span><span class="sxs-lookup"><span data-stu-id="a2e45-126">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: (All)
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e45-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="a2e45-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="a2e45-128">Müşteri tarafından tercih edilen destek dili.</span><span class="sxs-lookup"><span data-stu-id="a2e45-128">Customer preferred support language.</span></span>
<span data-ttu-id="a2e45-129">Burada listelenen desteklenen dillerden birinin geçerli bir dil-Contry kodu olması gerekir https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="a2e45-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e45-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="a2e45-130">-PreferredTimeZone</span></span>
<span data-ttu-id="a2e45-131">Müşterinin tercih ettiği saat dilimi.</span><span class="sxs-lookup"><span data-stu-id="a2e45-131">Customer preferred time zone.</span></span>
<span data-ttu-id="a2e45-132">Bu geçerli bir System.TimeZoneInfo.Id değeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a2e45-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e45-133">-Eldeki</span><span class="sxs-lookup"><span data-stu-id="a2e45-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="a2e45-134">Müşteri birincil e-posta adresi.</span><span class="sxs-lookup"><span data-stu-id="a2e45-134">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2e45-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="a2e45-135">-Confirm</span></span>
<span data-ttu-id="a2e45-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a2e45-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2e45-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2e45-137">-WhatIf</span></span>
<span data-ttu-id="a2e45-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2e45-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2e45-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a2e45-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2e45-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2e45-140">CommonParameters</span></span>
<span data-ttu-id="a2e45-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2e45-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2e45-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a2e45-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2e45-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2e45-143">INPUTS</span></span>

### <span data-ttu-id="a2e45-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a2e45-144">None</span></span>

## <span data-ttu-id="a2e45-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2e45-145">OUTPUTS</span></span>

### <span data-ttu-id="a2e45-146">Microsoft. Azure. Commands. support. model. PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="a2e45-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="a2e45-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2e45-147">NOTES</span></span>

## <span data-ttu-id="a2e45-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2e45-148">RELATED LINKS</span></span>
