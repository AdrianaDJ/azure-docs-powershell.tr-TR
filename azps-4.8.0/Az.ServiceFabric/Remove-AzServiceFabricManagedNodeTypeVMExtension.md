---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: dfe88add0571fe460520e7af3b8dece4c4d0bc6f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266329"
---
# <span data-ttu-id="49ec2-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="49ec2-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="49ec2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="49ec2-103">Düğüm türünden VM uzantısını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="49ec2-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="49ec2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49ec2-104">SYNTAX</span></span>

### <span data-ttu-id="49ec2-105">ByObj (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="49ec2-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ec2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="49ec2-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49ec2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="49ec2-107">DESCRIPTION</span></span>
<span data-ttu-id="49ec2-108">VM uzantısını ada göre düğüm türünden kaldırın.</span><span class="sxs-lookup"><span data-stu-id="49ec2-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="49ec2-109">[Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) kullanın ve VmExtensions özelliğine bakarak düğüm türündeki geçerli uzantıyı görün.</span><span class="sxs-lookup"><span data-stu-id="49ec2-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="49ec2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49ec2-110">EXAMPLES</span></span>

### <span data-ttu-id="49ec2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="49ec2-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="49ec2-112">Uzantıyı düğüm türünden ada göre kaldırma.</span><span class="sxs-lookup"><span data-stu-id="49ec2-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="49ec2-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="49ec2-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="49ec2-114">Şeridi kullanarak düğüm türünden ada göre uzantıyı kaldırın.</span><span class="sxs-lookup"><span data-stu-id="49ec2-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="49ec2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49ec2-115">PARAMETERS</span></span>

### <span data-ttu-id="49ec2-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="49ec2-116">-AsJob</span></span>
<span data-ttu-id="49ec2-117">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="49ec2-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="49ec2-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="49ec2-118">-ClusterName</span></span>
<span data-ttu-id="49ec2-119">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="49ec2-119">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ec2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ec2-120">-DefaultProfile</span></span>
<span data-ttu-id="49ec2-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="49ec2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49ec2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49ec2-122">-InputObject</span></span>
<span data-ttu-id="49ec2-123">Düğüm türü kaynağı</span><span class="sxs-lookup"><span data-stu-id="49ec2-123">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49ec2-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="49ec2-124">-Name</span></span>
<span data-ttu-id="49ec2-125">uzantı adı.</span><span class="sxs-lookup"><span data-stu-id="49ec2-125">extension name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ec2-126">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="49ec2-126">-NodeTypeName</span></span>
<span data-ttu-id="49ec2-127">Düğüm türünün adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="49ec2-127">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ec2-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="49ec2-128">-PassThru</span></span>
<span data-ttu-id="49ec2-129">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="49ec2-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="49ec2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49ec2-130">-ResourceGroupName</span></span>
<span data-ttu-id="49ec2-131">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="49ec2-131">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ec2-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="49ec2-132">-Confirm</span></span>
<span data-ttu-id="49ec2-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="49ec2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49ec2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49ec2-134">-WhatIf</span></span>
<span data-ttu-id="49ec2-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="49ec2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49ec2-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="49ec2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49ec2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ec2-137">CommonParameters</span></span>
<span data-ttu-id="49ec2-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49ec2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ec2-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="49ec2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ec2-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49ec2-140">INPUTS</span></span>

### <span data-ttu-id="49ec2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="49ec2-141">System.String</span></span>

## <span data-ttu-id="49ec2-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49ec2-142">OUTPUTS</span></span>

### <span data-ttu-id="49ec2-143">Microsoft. Azure. Commands. ServiceFabric. modeller. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="49ec2-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="49ec2-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49ec2-144">NOTES</span></span>

## <span data-ttu-id="49ec2-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49ec2-145">RELATED LINKS</span></span>
