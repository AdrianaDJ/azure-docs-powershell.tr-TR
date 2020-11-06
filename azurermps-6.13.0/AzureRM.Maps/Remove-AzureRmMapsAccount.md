---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/remove-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Remove-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Remove-AzureRmMapsAccount.md
ms.openlocfilehash: 9880bf574aec57796d185742b2f33b79da8f7c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588096"
---
# <span data-ttu-id="cc2ce-101">Remove-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="cc2ce-101">Remove-AzureRmMapsAccount</span></span>

## <span data-ttu-id="cc2ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc2ce-102">SYNOPSIS</span></span>
<span data-ttu-id="cc2ce-103">Azure haritalar hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-103">Deletes an Azure Maps account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc2ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cc2ce-104">SYNTAX</span></span>

### <span data-ttu-id="cc2ce-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cc2ce-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc2ce-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="cc2ce-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc2ce-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="cc2ce-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc2ce-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cc2ce-108">DESCRIPTION</span></span>
<span data-ttu-id="cc2ce-109">Remove-AzureRmMapsAccount cmdlet 'i belirtilen Azure haritalar hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-109">The Remove-AzureRmMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="cc2ce-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cc2ce-110">EXAMPLES</span></span>

### <span data-ttu-id="cc2ce-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cc2ce-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="cc2ce-112">MyResourceGroup kaynak grubundan MyAccount hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="cc2ce-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cc2ce-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="cc2ce-114">Belirtilen Azure haritalar hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="cc2ce-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cc2ce-115">PARAMETERS</span></span>

### <span data-ttu-id="cc2ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc2ce-116">-DefaultProfile</span></span>
<span data-ttu-id="cc2ce-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc2ce-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc2ce-118">-InputObject</span></span>
<span data-ttu-id="cc2ce-119">Get-AzureRmMapsAccount 'dan yöneltilen hesabı eşleştirir.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-119">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc2ce-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="cc2ce-120">-Name</span></span>
<span data-ttu-id="cc2ce-121">Harita hesap adı.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-121">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc2ce-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cc2ce-122">-PassThru</span></span>
<span data-ttu-id="cc2ce-123">Belirtilen hesabın başarıyla silinip silinmediğini döndürün.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-123">Return whether the specified account was successfully deleted or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc2ce-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc2ce-124">-ResourceGroupName</span></span>
<span data-ttu-id="cc2ce-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc2ce-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cc2ce-126">-ResourceId</span></span>
<span data-ttu-id="cc2ce-127">Hesap RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc2ce-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="cc2ce-128">-Confirm</span></span>
<span data-ttu-id="cc2ce-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc2ce-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc2ce-130">-WhatIf</span></span>
<span data-ttu-id="cc2ce-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc2ce-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc2ce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc2ce-133">CommonParameters</span></span>
<span data-ttu-id="cc2ce-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cc2ce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc2ce-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc2ce-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc2ce-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cc2ce-136">INPUTS</span></span>

### <span data-ttu-id="cc2ce-137">System. String</span><span class="sxs-lookup"><span data-stu-id="cc2ce-137">System.String</span></span>

### <span data-ttu-id="cc2ce-138">Microsoft. Azure. Commands. Map. model. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="cc2ce-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="cc2ce-139">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cc2ce-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="cc2ce-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cc2ce-140">OUTPUTS</span></span>

### <span data-ttu-id="cc2ce-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cc2ce-141">System.Boolean</span></span>

## <span data-ttu-id="cc2ce-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cc2ce-142">NOTES</span></span>

## <span data-ttu-id="cc2ce-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cc2ce-143">RELATED LINKS</span></span>
