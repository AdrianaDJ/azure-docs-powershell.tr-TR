---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 0fbf44e9a68a5cfaaea4138ec17caa2960a41e67
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108795"
---
# <span data-ttu-id="0fe47-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="0fe47-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="0fe47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fe47-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe47-103">Yeni bir eşleme hizmeti önekini kaldırır</span><span class="sxs-lookup"><span data-stu-id="0fe47-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="0fe47-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0fe47-104">SYNTAX</span></span>

### <span data-ttu-id="0fe47-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0fe47-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fe47-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0fe47-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fe47-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="0fe47-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fe47-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0fe47-108">DESCRIPTION</span></span>
<span data-ttu-id="0fe47-109">Eşleme hizmeti önekini eşleme hizmetinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0fe47-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="0fe47-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0fe47-110">EXAMPLES</span></span>

### <span data-ttu-id="0fe47-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0fe47-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="0fe47-112">Eşleme hizmeti nesnesinden önek kaldırma</span><span class="sxs-lookup"><span data-stu-id="0fe47-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="0fe47-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0fe47-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="0fe47-114">Eşleme hizmeti kaynak kimliğinden önek kaldırma.</span><span class="sxs-lookup"><span data-stu-id="0fe47-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="0fe47-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="0fe47-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="0fe47-116">Eşleme hizmeti kaynak grubu adı ve adından önek kaldırma</span><span class="sxs-lookup"><span data-stu-id="0fe47-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="0fe47-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0fe47-117">PARAMETERS</span></span>

### <span data-ttu-id="0fe47-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="0fe47-118">-AsJob</span></span>
<span data-ttu-id="0fe47-119">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="0fe47-119">Run in the background.</span></span>

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

### <span data-ttu-id="0fe47-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe47-120">-DefaultProfile</span></span>
<span data-ttu-id="0fe47-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0fe47-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fe47-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0fe47-122">-Force</span></span>
<span data-ttu-id="0fe47-123">İşlemin tamamlamasını zorunlu kılın</span><span class="sxs-lookup"><span data-stu-id="0fe47-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="0fe47-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fe47-124">-InputObject</span></span>
<span data-ttu-id="0fe47-125">Get-AzPeeringServicePrefix kullanma</span><span class="sxs-lookup"><span data-stu-id="0fe47-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe47-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="0fe47-126">-Name</span></span>
<span data-ttu-id="0fe47-127">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="0fe47-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="0fe47-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0fe47-128">-PassThru</span></span>
<span data-ttu-id="0fe47-129">Başarı için doğru ya da yanlış hatası döndürür.</span><span class="sxs-lookup"><span data-stu-id="0fe47-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="0fe47-130">-PrefixName</span><span class="sxs-lookup"><span data-stu-id="0fe47-130">-PrefixName</span></span>
<span data-ttu-id="0fe47-131">Önek adı.</span><span class="sxs-lookup"><span data-stu-id="0fe47-131">The name of prefix.</span></span>

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

### <span data-ttu-id="0fe47-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fe47-132">-ResourceGroupName</span></span>
<span data-ttu-id="0fe47-133">Var olan kaynak grubu adını oluştur veya kullan.</span><span class="sxs-lookup"><span data-stu-id="0fe47-133">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="0fe47-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0fe47-134">-ResourceId</span></span>
<span data-ttu-id="0fe47-135">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="0fe47-135">The resource id string name.</span></span>

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

### <span data-ttu-id="0fe47-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="0fe47-136">-Confirm</span></span>
<span data-ttu-id="0fe47-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0fe47-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fe47-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fe47-138">-WhatIf</span></span>
<span data-ttu-id="0fe47-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0fe47-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fe47-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0fe47-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fe47-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe47-141">CommonParameters</span></span>
<span data-ttu-id="0fe47-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0fe47-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe47-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0fe47-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe47-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0fe47-144">INPUTS</span></span>

### <span data-ttu-id="0fe47-145">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fe47-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="0fe47-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0fe47-146">System.String</span></span>

## <span data-ttu-id="0fe47-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0fe47-147">OUTPUTS</span></span>

### <span data-ttu-id="0fe47-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0fe47-148">System.Boolean</span></span>

## <span data-ttu-id="0fe47-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0fe47-149">NOTES</span></span>

## <span data-ttu-id="0fe47-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0fe47-150">RELATED LINKS</span></span>
