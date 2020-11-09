---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
ms.openlocfilehash: d7e8c65a54adae1de7b7f3ba1ed2d67139638846
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322050"
---
# <span data-ttu-id="cf6ec-101">Invoke-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cf6ec-101">Invoke-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="cf6ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf6ec-102">SYNOPSIS</span></span>
<span data-ttu-id="cf6ec-103">Bir depolama kapsayıcısında belirli eylemleri çağırır</span><span class="sxs-lookup"><span data-stu-id="cf6ec-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="cf6ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf6ec-104">SYNTAX</span></span>

### <span data-ttu-id="cf6ec-105">Invokebynameparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cf6ec-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf6ec-106">Invokebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="cf6ec-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf6ec-107">Invokebyinputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="cf6ec-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf6ec-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf6ec-108">DESCRIPTION</span></span>
<span data-ttu-id="cf6ec-109">**Invoke-AzStackEdgeStorageContainer** cmdlet 'ı, yığın uç aygıtındaki bir depolama kapsayıcısındaki verileri yenilemeye yönelik eylemleri çağırır.</span><span class="sxs-lookup"><span data-stu-id="cf6ec-109">The **Invoke-AzStackEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Stack Edge device.</span></span> 

## <span data-ttu-id="cf6ec-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf6ec-110">EXAMPLES</span></span>

### <span data-ttu-id="cf6ec-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cf6ec-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="cf6ec-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cf6ec-112">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzStackEdgeStorageContainer
```

## <span data-ttu-id="cf6ec-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf6ec-113">PARAMETERS</span></span>

### <span data-ttu-id="cf6ec-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="cf6ec-114">-AsJob</span></span>
<span data-ttu-id="cf6ec-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cf6ec-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf6ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf6ec-116">-DefaultProfile</span></span>
<span data-ttu-id="cf6ec-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cf6ec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf6ec-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="cf6ec-118">-DeviceName</span></span>
<span data-ttu-id="cf6ec-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="cf6ec-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf6ec-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cf6ec-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="cf6ec-121">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="cf6ec-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf6ec-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf6ec-122">-InputObject</span></span>
<span data-ttu-id="cf6ec-123">Var olan EdgeStorageAccount nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="cf6ec-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf6ec-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="cf6ec-124">-Name</span></span>
<span data-ttu-id="cf6ec-125">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="cf6ec-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf6ec-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cf6ec-126">-PassThru</span></span>
<span data-ttu-id="cf6ec-127">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="cf6ec-127">returns true if successful</span></span>

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

### <span data-ttu-id="cf6ec-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="cf6ec-128">-RefreshData</span></span>
<span data-ttu-id="cf6ec-129">Buluttan verilerle kapsayıcı meta verilerini yenileme</span><span class="sxs-lookup"><span data-stu-id="cf6ec-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="cf6ec-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf6ec-130">-ResourceGroupName</span></span>
<span data-ttu-id="cf6ec-131">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="cf6ec-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf6ec-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cf6ec-132">-ResourceId</span></span>
<span data-ttu-id="cf6ec-133">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cf6ec-133">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf6ec-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="cf6ec-134">-Confirm</span></span>
<span data-ttu-id="cf6ec-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cf6ec-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf6ec-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf6ec-136">-WhatIf</span></span>
<span data-ttu-id="cf6ec-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf6ec-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf6ec-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cf6ec-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf6ec-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf6ec-139">CommonParameters</span></span>
<span data-ttu-id="cf6ec-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf6ec-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf6ec-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cf6ec-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf6ec-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf6ec-142">INPUTS</span></span>

### <span data-ttu-id="cf6ec-143">System. String</span><span class="sxs-lookup"><span data-stu-id="cf6ec-143">System.String</span></span>

### <span data-ttu-id="cf6ec-144">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cf6ec-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="cf6ec-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf6ec-145">OUTPUTS</span></span>

### <span data-ttu-id="cf6ec-146">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cf6ec-146">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="cf6ec-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf6ec-147">NOTES</span></span>

## <span data-ttu-id="cf6ec-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf6ec-148">RELATED LINKS</span></span>
