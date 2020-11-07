---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: c228b00cb8d0d1e8f238e0b2e75427e0d623490f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936772"
---
# <span data-ttu-id="059fb-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="059fb-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="059fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="059fb-102">SYNOPSIS</span></span>
<span data-ttu-id="059fb-103">Bir depolama kapsayıcısında belirli eylemleri çağırır</span><span class="sxs-lookup"><span data-stu-id="059fb-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="059fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="059fb-104">SYNTAX</span></span>

### <span data-ttu-id="059fb-105">Invokebynameparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="059fb-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="059fb-106">Invokebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="059fb-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="059fb-107">Invokebyinputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="059fb-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="059fb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="059fb-108">DESCRIPTION</span></span>
<span data-ttu-id="059fb-109">**Invoke-AzDataBoxEdgeStorageContainer** cmdlet 'i, bir veri kutusu uç aygıtındaki bir depolama kapsayıcısındaki verileri yenilemeye yönelik eylemleri başlatır.</span><span class="sxs-lookup"><span data-stu-id="059fb-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="059fb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="059fb-110">EXAMPLES</span></span>

### <span data-ttu-id="059fb-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="059fb-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="059fb-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="059fb-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="059fb-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="059fb-113">PARAMETERS</span></span>

### <span data-ttu-id="059fb-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="059fb-114">-AsJob</span></span>
<span data-ttu-id="059fb-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="059fb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="059fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059fb-116">-DefaultProfile</span></span>
<span data-ttu-id="059fb-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="059fb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="059fb-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="059fb-118">-DeviceName</span></span>
<span data-ttu-id="059fb-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="059fb-119">Device Name</span></span>

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

### <span data-ttu-id="059fb-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="059fb-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="059fb-121">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="059fb-121">Resource Name</span></span>

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

### <span data-ttu-id="059fb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="059fb-122">-InputObject</span></span>
<span data-ttu-id="059fb-123">Var olan EdgeStorageAccount nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="059fb-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="059fb-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="059fb-124">-Name</span></span>
<span data-ttu-id="059fb-125">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="059fb-125">Resource Name</span></span>

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

### <span data-ttu-id="059fb-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="059fb-126">-PassThru</span></span>
<span data-ttu-id="059fb-127">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="059fb-127">returns true if successful</span></span>

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

### <span data-ttu-id="059fb-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="059fb-128">-RefreshData</span></span>
<span data-ttu-id="059fb-129">Buluttan verilerle kapsayıcı meta verilerini yenileme</span><span class="sxs-lookup"><span data-stu-id="059fb-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="059fb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="059fb-130">-ResourceGroupName</span></span>
<span data-ttu-id="059fb-131">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="059fb-131">Resource Group Name</span></span>

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

### <span data-ttu-id="059fb-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="059fb-132">-ResourceId</span></span>
<span data-ttu-id="059fb-133">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="059fb-133">Azure ResourceId</span></span>

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

### <span data-ttu-id="059fb-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="059fb-134">-Confirm</span></span>
<span data-ttu-id="059fb-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="059fb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="059fb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="059fb-136">-WhatIf</span></span>
<span data-ttu-id="059fb-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="059fb-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="059fb-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="059fb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="059fb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059fb-139">CommonParameters</span></span>
<span data-ttu-id="059fb-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="059fb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059fb-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="059fb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059fb-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="059fb-142">INPUTS</span></span>

### <span data-ttu-id="059fb-143">System. String</span><span class="sxs-lookup"><span data-stu-id="059fb-143">System.String</span></span>

### <span data-ttu-id="059fb-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="059fb-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="059fb-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="059fb-145">OUTPUTS</span></span>

### <span data-ttu-id="059fb-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="059fb-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="059fb-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="059fb-147">NOTES</span></span>

## <span data-ttu-id="059fb-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="059fb-148">RELATED LINKS</span></span>
