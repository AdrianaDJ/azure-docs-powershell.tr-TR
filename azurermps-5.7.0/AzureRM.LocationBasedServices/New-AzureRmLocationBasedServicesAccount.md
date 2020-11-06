---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 739ce121e26f1010c5c13ff3330dadffa02053af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588205"
---
# <span data-ttu-id="97eac-101">New-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="97eac-101">New-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="97eac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97eac-102">SYNOPSIS</span></span>
<span data-ttu-id="97eac-103">Konum tabanlı hizmetler hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97eac-103">Creates a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97eac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97eac-104">SYNTAX</span></span>

```
New-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97eac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="97eac-105">DESCRIPTION</span></span>
<span data-ttu-id="97eac-106">**New-Azurermlocationbasevseçservicesaccount** cmdlet 'i belirtilen SKU 'ya sahip bir konum tabanlı hizmetler hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97eac-106">The **New-AzureRmLocationBasedServicesAccount** cmdlet creates a Location Based Services account with the specified SKU.</span></span>

## <span data-ttu-id="97eac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97eac-107">EXAMPLES</span></span>

### <span data-ttu-id="97eac-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="97eac-108">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

Notice
By creating a Location Based Account, you are consenting to the terms of use (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): y

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="97eac-109">MyResourceGroup kaynak grubunda MyAccount adlı yeni bir konum tabanlı hizmetler hesabı SKU S0 ve bir etiketle oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="97eac-109">Creates a new Location Based Services account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="97eac-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97eac-110">PARAMETERS</span></span>

### <span data-ttu-id="97eac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97eac-111">-DefaultProfile</span></span>
<span data-ttu-id="97eac-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97eac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eac-113">-Force</span><span class="sxs-lookup"><span data-stu-id="97eac-113">-Force</span></span>
<span data-ttu-id="97eac-114">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="97eac-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eac-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="97eac-115">-Name</span></span>
<span data-ttu-id="97eac-116">Konum tabanlı hizmetler hesap adı.</span><span class="sxs-lookup"><span data-stu-id="97eac-116">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97eac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97eac-117">-ResourceGroupName</span></span>
<span data-ttu-id="97eac-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="97eac-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97eac-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="97eac-119">-SkuName</span></span>
<span data-ttu-id="97eac-120">Konum tabanlı hizmetler hesap SKU adı.</span><span class="sxs-lookup"><span data-stu-id="97eac-120">Location Based Services Account Sku Name.</span></span>

<span data-ttu-id="97eac-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="97eac-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="97eac-122">S0</span><span class="sxs-lookup"><span data-stu-id="97eac-122">S0</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: S0

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97eac-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="97eac-123">-Tag</span></span>
<span data-ttu-id="97eac-124">Konum temelli hizmetler hesap etiketleri.</span><span class="sxs-lookup"><span data-stu-id="97eac-124">Location Based Services Account Tags.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eac-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="97eac-125">-Confirm</span></span>
<span data-ttu-id="97eac-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97eac-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eac-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97eac-127">-WhatIf</span></span>
<span data-ttu-id="97eac-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97eac-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97eac-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97eac-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97eac-130">CommonParameters</span></span>
<span data-ttu-id="97eac-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97eac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97eac-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97eac-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97eac-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97eac-133">INPUTS</span></span>

### <span data-ttu-id="97eac-134">System. String</span><span class="sxs-lookup"><span data-stu-id="97eac-134">System.String</span></span>

## <span data-ttu-id="97eac-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97eac-135">OUTPUTS</span></span>

### <span data-ttu-id="97eac-136">Microsoft. Azure. Commands. Locationbasevseçservices. model. Pslocationbasevseçservicesaccount</span><span class="sxs-lookup"><span data-stu-id="97eac-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>

## <span data-ttu-id="97eac-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97eac-137">NOTES</span></span>

<span data-ttu-id="97eac-138">Konum tabanlı hizmetler hesabı oluşturmak, koşulları kabul etmek için bir istem yanıtlamayı gerektirir (bkz https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/) .</span><span class="sxs-lookup"><span data-stu-id="97eac-138">Creating a Location Based Services account requires answering a prompt to accept terms (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).</span></span>  <span data-ttu-id="97eac-139">-Force parametresi, terimlerin kabul edilmesi gerektiğini belirtmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="97eac-139">The -Force parameter can be used to indicate acceptance of the terms.</span></span>

## <span data-ttu-id="97eac-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97eac-140">RELATED LINKS</span></span>
