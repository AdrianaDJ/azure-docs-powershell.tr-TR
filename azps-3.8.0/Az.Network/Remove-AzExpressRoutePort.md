---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: 7e6ee711de551de00a54930be2bdb285998e3ccb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104053"
---
# <span data-ttu-id="3a5a6-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3a5a6-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="3a5a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a5a6-102">SYNOPSIS</span></span>
<span data-ttu-id="3a5a6-103">ExpressRoutePort öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a5a6-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="3a5a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a5a6-104">SYNTAX</span></span>

### <span data-ttu-id="3a5a6-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3a5a6-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a5a6-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="3a5a6-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a5a6-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3a5a6-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a5a6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a5a6-108">DESCRIPTION</span></span>
<span data-ttu-id="3a5a6-109">**Remove-AzExpressRoutePort** cmdlet 'ı bir expressrouteport öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a5a6-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="3a5a6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a5a6-110">EXAMPLES</span></span>

### <span data-ttu-id="3a5a6-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3a5a6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="3a5a6-112">Aboneliğinizdeki $rg kaynak grubunda ExpressRoutePort kaynağını $PortName kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a5a6-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="3a5a6-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3a5a6-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="3a5a6-114">InputObject içindeki ExpressRoutePort kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a5a6-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="3a5a6-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3a5a6-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="3a5a6-116">RESOURCEID $id ile ExpressRoutePort kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a5a6-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="3a5a6-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a5a6-117">PARAMETERS</span></span>

### <span data-ttu-id="3a5a6-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="3a5a6-118">-AsJob</span></span>
<span data-ttu-id="3a5a6-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3a5a6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a5a6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a5a6-120">-DefaultProfile</span></span>
<span data-ttu-id="3a5a6-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a5a6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a5a6-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3a5a6-122">-Force</span></span>
<span data-ttu-id="3a5a6-123">Kaynağı silmek istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="3a5a6-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="3a5a6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a5a6-124">-InputObject</span></span>
<span data-ttu-id="3a5a6-125">Hızlı rota bağlantı noktası nesnesi</span><span class="sxs-lookup"><span data-stu-id="3a5a6-125">The express route port object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a5a6-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a5a6-126">-Name</span></span>
<span data-ttu-id="3a5a6-127">ExpressRoutePort adı.</span><span class="sxs-lookup"><span data-stu-id="3a5a6-127">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a5a6-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3a5a6-128">-PassThru</span></span>
<span data-ttu-id="3a5a6-129">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="3a5a6-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="3a5a6-130">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="3a5a6-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a5a6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a5a6-131">-ResourceGroupName</span></span>
<span data-ttu-id="3a5a6-132">ExpressRoutePort kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3a5a6-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a5a6-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3a5a6-133">-ResourceId</span></span>
<span data-ttu-id="3a5a6-134">Hızlı rota bağlantı noktasının RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="3a5a6-134">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a5a6-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a5a6-135">-Confirm</span></span>
<span data-ttu-id="3a5a6-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a5a6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a5a6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a5a6-137">-WhatIf</span></span>
<span data-ttu-id="3a5a6-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a5a6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a5a6-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a5a6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a5a6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a5a6-140">CommonParameters</span></span>
<span data-ttu-id="3a5a6-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a5a6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a5a6-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a5a6-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a5a6-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a5a6-143">INPUTS</span></span>

### <span data-ttu-id="3a5a6-144">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3a5a6-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="3a5a6-145">System. String</span><span class="sxs-lookup"><span data-stu-id="3a5a6-145">System.String</span></span>

## <span data-ttu-id="3a5a6-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a5a6-146">OUTPUTS</span></span>

### <span data-ttu-id="3a5a6-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3a5a6-147">System.Boolean</span></span>

## <span data-ttu-id="3a5a6-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a5a6-148">NOTES</span></span>

## <span data-ttu-id="3a5a6-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a5a6-149">RELATED LINKS</span></span>

[<span data-ttu-id="3a5a6-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3a5a6-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="3a5a6-151">Yeni-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3a5a6-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="3a5a6-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3a5a6-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
