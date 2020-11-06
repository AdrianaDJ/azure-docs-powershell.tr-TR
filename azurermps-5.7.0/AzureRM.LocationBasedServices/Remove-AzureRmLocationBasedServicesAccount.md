---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/remove-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 0496fcdba082370654b3259f101987d1a78621fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592486"
---
# <span data-ttu-id="7f6aa-101">Remove-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7f6aa-101">Remove-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="7f6aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f6aa-102">SYNOPSIS</span></span>
<span data-ttu-id="7f6aa-103">Konum tabanlı hizmetler hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="7f6aa-103">Deletes a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f6aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f6aa-104">SYNTAX</span></span>

### <span data-ttu-id="7f6aa-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7f6aa-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f6aa-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="7f6aa-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f6aa-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="7f6aa-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f6aa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f6aa-108">DESCRIPTION</span></span>
<span data-ttu-id="7f6aa-109">**Remove-Azurermlocationbasevseçservicesaccount** cmdlet 'ı belirtilen konum tabanlı hizmetler hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="7f6aa-109">The **Remove-AzureRmLocationBasedServicesAccount** cmdlet deletes the specified Location Based Services account.</span></span>

## <span data-ttu-id="7f6aa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f6aa-110">EXAMPLES</span></span>

### <span data-ttu-id="7f6aa-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7f6aa-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="7f6aa-112">MyResourceGroup kaynak grubundan MyAccount hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="7f6aa-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="7f6aa-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7f6aa-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="7f6aa-114">Belirtilen konum tabanlı hizmetler hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="7f6aa-114">Deletes the specified Location Based Services Account.</span></span>

## <span data-ttu-id="7f6aa-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f6aa-115">PARAMETERS</span></span>

### <span data-ttu-id="7f6aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f6aa-116">-DefaultProfile</span></span>
<span data-ttu-id="7f6aa-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f6aa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f6aa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f6aa-118">-InputObject</span></span>
<span data-ttu-id="7f6aa-119">[Get-Azurermlocationbasevseçservicesaccount](Get-AzureRmLocationBasedServicesAccount.md)'dan yöneltilen konum tabanlı hizmetler hesabı.</span><span class="sxs-lookup"><span data-stu-id="7f6aa-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f6aa-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="7f6aa-120">-Name</span></span>
<span data-ttu-id="7f6aa-121">Konum tabanlı hizmetler hesap adı.</span><span class="sxs-lookup"><span data-stu-id="7f6aa-121">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f6aa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f6aa-122">-ResourceGroupName</span></span>
<span data-ttu-id="7f6aa-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7f6aa-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f6aa-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7f6aa-124">-ResourceId</span></span>
<span data-ttu-id="7f6aa-125">Konum temelli hizmetler hesabı RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="7f6aa-125">Location Based Services Account ResourceId.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f6aa-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f6aa-126">-Confirm</span></span>
<span data-ttu-id="7f6aa-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f6aa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f6aa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f6aa-128">-WhatIf</span></span>
<span data-ttu-id="7f6aa-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f6aa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f6aa-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f6aa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f6aa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f6aa-131">CommonParameters</span></span>
<span data-ttu-id="7f6aa-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f6aa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f6aa-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f6aa-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f6aa-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f6aa-134">INPUTS</span></span>

### <span data-ttu-id="7f6aa-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7f6aa-135">System.String</span></span>

## <span data-ttu-id="7f6aa-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f6aa-136">OUTPUTS</span></span>

### <span data-ttu-id="7f6aa-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="7f6aa-137">System.Object</span></span>

## <span data-ttu-id="7f6aa-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f6aa-138">NOTES</span></span>

## <span data-ttu-id="7f6aa-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f6aa-139">RELATED LINKS</span></span>
