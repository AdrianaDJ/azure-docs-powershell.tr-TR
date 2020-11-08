---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/remove-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
ms.openlocfilehash: b84a5d6cbbf090243a63ad9919a3fbb1977d77f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274458"
---
# <span data-ttu-id="c3d36-101">Remove-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="c3d36-101">Remove-AzMapsAccount</span></span>

## <span data-ttu-id="c3d36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3d36-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d36-103">Azure haritalar hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="c3d36-103">Deletes an Azure Maps account.</span></span>

## <span data-ttu-id="c3d36-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3d36-104">SYNTAX</span></span>

### <span data-ttu-id="c3d36-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c3d36-105">NameParameterSet (Default)</span></span>
```
Remove-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3d36-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="c3d36-106">InputObjectParameterSet</span></span>
```
Remove-AzMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3d36-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c3d36-107">ResourceIdParameterSet</span></span>
```
Remove-AzMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3d36-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3d36-108">DESCRIPTION</span></span>
<span data-ttu-id="c3d36-109">Remove-AzMapsAccount cmdlet 'i belirtilen Azure haritalar hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="c3d36-109">The Remove-AzMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="c3d36-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3d36-110">EXAMPLES</span></span>

### <span data-ttu-id="c3d36-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c3d36-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="c3d36-112">MyResourceGroup kaynak grubundan MyAccount hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="c3d36-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="c3d36-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c3d36-113">Example 2</span></span>
```
PS C:\> Remove-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="c3d36-114">Belirtilen Azure haritalar hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="c3d36-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="c3d36-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3d36-115">PARAMETERS</span></span>

### <span data-ttu-id="c3d36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d36-116">-DefaultProfile</span></span>
<span data-ttu-id="c3d36-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c3d36-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3d36-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3d36-118">-InputObject</span></span>
<span data-ttu-id="c3d36-119">Get-AzMapsAccount 'dan yöneltilen hesabı eşleştirir.</span><span class="sxs-lookup"><span data-stu-id="c3d36-119">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="c3d36-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="c3d36-120">-Name</span></span>
<span data-ttu-id="c3d36-121">Harita hesap adı.</span><span class="sxs-lookup"><span data-stu-id="c3d36-121">Maps Account Name.</span></span>

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

### <span data-ttu-id="c3d36-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c3d36-122">-PassThru</span></span>
<span data-ttu-id="c3d36-123">Belirtilen hesabın başarıyla silinip silinmediğini döndürün.</span><span class="sxs-lookup"><span data-stu-id="c3d36-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="c3d36-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3d36-124">-ResourceGroupName</span></span>
<span data-ttu-id="c3d36-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c3d36-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c3d36-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c3d36-126">-ResourceId</span></span>
<span data-ttu-id="c3d36-127">Hesap RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="c3d36-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="c3d36-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="c3d36-128">-Confirm</span></span>
<span data-ttu-id="c3d36-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c3d36-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3d36-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3d36-130">-WhatIf</span></span>
<span data-ttu-id="c3d36-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c3d36-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3d36-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c3d36-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3d36-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d36-133">CommonParameters</span></span>
<span data-ttu-id="c3d36-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3d36-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d36-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3d36-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d36-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3d36-136">INPUTS</span></span>

### <span data-ttu-id="c3d36-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c3d36-137">System.String</span></span>

### <span data-ttu-id="c3d36-138">Microsoft. Azure. Commands. Map. model. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="c3d36-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="c3d36-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3d36-139">OUTPUTS</span></span>

### <span data-ttu-id="c3d36-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c3d36-140">System.Boolean</span></span>

## <span data-ttu-id="c3d36-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3d36-141">NOTES</span></span>

## <span data-ttu-id="c3d36-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3d36-142">RELATED LINKS</span></span>
