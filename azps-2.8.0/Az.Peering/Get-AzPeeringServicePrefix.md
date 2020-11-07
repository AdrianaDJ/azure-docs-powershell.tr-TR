---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
ms.openlocfilehash: 4bbd6e491d67e9ef3dd4fae0adc92561aa01c866
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932859"
---
# <span data-ttu-id="8e039-101">Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="8e039-101">Get-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="8e039-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e039-102">SYNOPSIS</span></span>
<span data-ttu-id="8e039-103">Aboneliğin eşleme hizmeti öneklerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="8e039-103">Gets a list of peering service prefixes for a subscription.</span></span>

## <span data-ttu-id="8e039-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e039-104">SYNTAX</span></span>

### <span data-ttu-id="8e039-105">ByResourceGroupAndName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8e039-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name <String>]
 [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e039-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="8e039-106">Default</span></span>
```
Get-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name <String>] [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e039-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="8e039-107">ByResourceId</span></span>
```
Get-AzPeeringServicePrefix [-ResourceId] <String> [-Expand] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e039-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e039-108">DESCRIPTION</span></span>
<span data-ttu-id="8e039-109">Eşleme hizmeti nesneleri için liste eşleme hizmeti önekleri</span><span class="sxs-lookup"><span data-stu-id="8e039-109">List peering service prefixes for peering service objects</span></span>

## <span data-ttu-id="8e039-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e039-110">EXAMPLES</span></span>

### <span data-ttu-id="8e039-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8e039-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name | Get-AzPeeringServicePrefix

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes

Prefix                : 200.25.71.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix3463
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService4084/pre
                        fixes/myPrefix3463
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="8e039-112">Bir eşleme hizmetinin öneklerini boru komutlarına dayalı olarak alır.</span><span class="sxs-lookup"><span data-stu-id="8e039-112">Gets the prefixes for a peering service based on piping commands.</span></span>

### <span data-ttu-id="8e039-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8e039-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceId $peeringServicePrefixResourceId 

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="8e039-114">Kaynak kimliğiyle bir eşleme hizmeti için belirli bir önek alır.</span><span class="sxs-lookup"><span data-stu-id="8e039-114">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="8e039-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="8e039-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="8e039-116">Kaynak kimliğiyle bir eşleme hizmeti için belirli bir önek alır.</span><span class="sxs-lookup"><span data-stu-id="8e039-116">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="8e039-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="8e039-117">Example 4</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName -Expand

Prefix                : 10.2.6.0/24
PrefixValidationState : Failed
LearnedType           : None
ErrorMessage          :
Events                : {}
ProvisioningState     : Succeeded
Name                  : ps0
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService6616/pre
                        fixes/ps0
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="8e039-118">Genişletilmiş öznitelikleri olan bir eşleme hizmeti için belirli bir önek alır</span><span class="sxs-lookup"><span data-stu-id="8e039-118">Gets a specific prefix for a peering service with expanded attributes</span></span>

## <span data-ttu-id="8e039-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e039-119">PARAMETERS</span></span>

### <span data-ttu-id="8e039-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e039-120">-DefaultProfile</span></span>
<span data-ttu-id="8e039-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e039-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e039-122">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="8e039-122">-Expand</span></span>
<span data-ttu-id="8e039-123">Eşleme hizmeti öneki için olayları görüntüleme</span><span class="sxs-lookup"><span data-stu-id="8e039-123">View the events for a peering service prefix</span></span>

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

### <span data-ttu-id="8e039-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="8e039-124">-Name</span></span>
<span data-ttu-id="8e039-125">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="8e039-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e039-126">-Peeringhizmetadı</span><span class="sxs-lookup"><span data-stu-id="8e039-126">-PeeringServiceName</span></span>
<span data-ttu-id="8e039-127">Eşleme hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="8e039-127">The peering service name.</span></span> <span data-ttu-id="8e039-128">Yeni bir eşleme hizmeti Get-AzPeeringService veya liste için New-AzPeeringService cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="8e039-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e039-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="8e039-129">-PeeringServiceObject</span></span>
<span data-ttu-id="8e039-130">Get-AzPeeringService kullanma</span><span class="sxs-lookup"><span data-stu-id="8e039-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e039-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e039-131">-ResourceGroupName</span></span>
<span data-ttu-id="8e039-132">Var olan kaynak grubu adını oluştur veya kullan.</span><span class="sxs-lookup"><span data-stu-id="8e039-132">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e039-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8e039-133">-ResourceId</span></span>
<span data-ttu-id="8e039-134">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="8e039-134">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e039-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e039-135">CommonParameters</span></span>
<span data-ttu-id="8e039-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e039-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e039-137">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8e039-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e039-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e039-138">INPUTS</span></span>

### <span data-ttu-id="8e039-139">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e039-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

### <span data-ttu-id="8e039-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8e039-140">System.String</span></span>

## <span data-ttu-id="8e039-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e039-141">OUTPUTS</span></span>

### <span data-ttu-id="8e039-142">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e039-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="8e039-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e039-143">NOTES</span></span>

## <span data-ttu-id="8e039-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e039-144">RELATED LINKS</span></span>
