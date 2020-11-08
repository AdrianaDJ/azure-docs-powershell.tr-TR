---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 36003d1fbca7566ae663a1d878386f3d8d67f484
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932839"
---
# <span data-ttu-id="55498-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="55498-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="55498-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55498-102">SYNOPSIS</span></span>
<span data-ttu-id="55498-103">Yeni bir eşleme hizmeti önekini kaldırır</span><span class="sxs-lookup"><span data-stu-id="55498-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="55498-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55498-104">SYNTAX</span></span>

### <span data-ttu-id="55498-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="55498-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PeeringServiceName] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55498-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="55498-106">Default</span></span>
```
Remove-AzPeeringServicePrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55498-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="55498-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55498-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="55498-108">DESCRIPTION</span></span>
<span data-ttu-id="55498-109">Eşleme hizmeti önekini eşleme hizmetinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="55498-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="55498-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55498-110">EXAMPLES</span></span>

### <span data-ttu-id="55498-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="55498-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="55498-112">Eşleme hizmeti nesnesinden önek kaldırma</span><span class="sxs-lookup"><span data-stu-id="55498-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="55498-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="55498-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="55498-114">Eşleme hizmeti kaynak kimliğinden önek kaldırma.</span><span class="sxs-lookup"><span data-stu-id="55498-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="55498-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="55498-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="55498-116">Eşleme hizmeti kaynak grubu adı ve adından önek kaldırma</span><span class="sxs-lookup"><span data-stu-id="55498-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="55498-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55498-117">PARAMETERS</span></span>

### <span data-ttu-id="55498-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="55498-118">-AsJob</span></span>
<span data-ttu-id="55498-119">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="55498-119">Run in the background.</span></span>

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

### <span data-ttu-id="55498-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55498-120">-DefaultProfile</span></span>
<span data-ttu-id="55498-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55498-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55498-122">-Force</span><span class="sxs-lookup"><span data-stu-id="55498-122">-Force</span></span>
<span data-ttu-id="55498-123">İşlemin tamamlamasını zorunlu kılın</span><span class="sxs-lookup"><span data-stu-id="55498-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="55498-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55498-124">-InputObject</span></span>
<span data-ttu-id="55498-125">Get-AzPeeringServicePrefix kullanma</span><span class="sxs-lookup"><span data-stu-id="55498-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55498-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="55498-126">-Name</span></span>
<span data-ttu-id="55498-127">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="55498-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55498-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="55498-128">-PassThru</span></span>
<span data-ttu-id="55498-129">Başarı için doğru ya da yanlış hatası döndürür.</span><span class="sxs-lookup"><span data-stu-id="55498-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="55498-130">-Peeringhizmetadı</span><span class="sxs-lookup"><span data-stu-id="55498-130">-PeeringServiceName</span></span>
<span data-ttu-id="55498-131">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="55498-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55498-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55498-132">-ResourceGroupName</span></span>
<span data-ttu-id="55498-133">Var olan kaynak grubu adını oluştur veya kullan.</span><span class="sxs-lookup"><span data-stu-id="55498-133">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55498-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="55498-134">-ResourceId</span></span>
<span data-ttu-id="55498-135">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="55498-135">The resource id string name.</span></span>

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

### <span data-ttu-id="55498-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="55498-136">-Confirm</span></span>
<span data-ttu-id="55498-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55498-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55498-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55498-138">-WhatIf</span></span>
<span data-ttu-id="55498-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55498-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55498-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55498-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55498-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55498-141">CommonParameters</span></span>
<span data-ttu-id="55498-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55498-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55498-143">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="55498-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55498-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55498-144">INPUTS</span></span>

### <span data-ttu-id="55498-145">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55498-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="55498-146">System. String</span><span class="sxs-lookup"><span data-stu-id="55498-146">System.String</span></span>

## <span data-ttu-id="55498-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55498-147">OUTPUTS</span></span>

### <span data-ttu-id="55498-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55498-148">System.Boolean</span></span>

## <span data-ttu-id="55498-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55498-149">NOTES</span></span>

## <span data-ttu-id="55498-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55498-150">RELATED LINKS</span></span>