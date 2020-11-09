---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 29bf8cf612d3569480c62784466879095ebcdb6e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321202"
---
# <span data-ttu-id="94e11-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="94e11-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="94e11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94e11-102">SYNOPSIS</span></span>
<span data-ttu-id="94e11-103">Cihazda belirli eylemleri başlatır.</span><span class="sxs-lookup"><span data-stu-id="94e11-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="94e11-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94e11-104">SYNTAX</span></span>

### <span data-ttu-id="94e11-105">InvokeScanForUpdateParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="94e11-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e11-106">Invokefetchupdatesbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="94e11-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e11-107">Invokeınstallupdatesbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="94e11-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e11-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94e11-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e11-109">Invokeınstallupdateparameterset</span><span class="sxs-lookup"><span data-stu-id="94e11-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e11-110">Invokefetchupdateparameterset</span><span class="sxs-lookup"><span data-stu-id="94e11-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e11-111">Invokefetchupdatesbydeviceobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="94e11-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e11-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94e11-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e11-113">Invokeınstallupdatesbydeviceobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="94e11-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94e11-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="94e11-114">DESCRIPTION</span></span>
<span data-ttu-id="94e11-115">**Invoke-AzDataBoxEdgeDevice** cmdlet 'ı, veri kutusu Edge cihazında güncelleştirmeleri taramak, indirmek ve yüklemek için eylemleri çağırır.</span><span class="sxs-lookup"><span data-stu-id="94e11-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="94e11-116">Otomatik tarama cihazda günlük olarak çalışır, bu cmdlet 'i çalıştırarak taramayı açıkça tetikleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94e11-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="94e11-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94e11-117">EXAMPLES</span></span>

### <span data-ttu-id="94e11-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="94e11-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="94e11-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="94e11-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="94e11-120">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="94e11-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="94e11-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94e11-121">PARAMETERS</span></span>

### <span data-ttu-id="94e11-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="94e11-122">-AsJob</span></span>
<span data-ttu-id="94e11-123">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="94e11-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94e11-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e11-124">-DefaultProfile</span></span>
<span data-ttu-id="94e11-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94e11-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94e11-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="94e11-126">-DeviceObject</span></span>
<span data-ttu-id="94e11-127">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="94e11-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e11-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="94e11-128">-FetchUpdate</span></span>
<span data-ttu-id="94e11-129">Veri kutusu kenarı/ağ geçidi cihazında güncelleştirmeleri indirir</span><span class="sxs-lookup"><span data-stu-id="94e11-129">Downloads the updates on a data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeFetchUpdateParameterSet, InvokeFetchUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e11-130">-Installupdate</span><span class="sxs-lookup"><span data-stu-id="94e11-130">-InstallUpdate</span></span>
<span data-ttu-id="94e11-131">Veri kutusu kenarı/ağ geçidi cihazında güncelleştirmeleri yükler</span><span class="sxs-lookup"><span data-stu-id="94e11-131">Installs the updates on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeInstallUpdatesByResourceIdParameterSet, InvokeInstallUpdateParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e11-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="94e11-132">-Name</span></span>
<span data-ttu-id="94e11-133">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="94e11-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e11-134">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="94e11-134">-PassThru</span></span>
<span data-ttu-id="94e11-135">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="94e11-135">returns true if successful</span></span>

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

### <span data-ttu-id="94e11-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94e11-136">-ResourceGroupName</span></span>
<span data-ttu-id="94e11-137">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="94e11-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e11-138">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="94e11-138">-ResourceId</span></span>
<span data-ttu-id="94e11-139">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="94e11-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e11-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="94e11-140">-ScanForUpdate</span></span>
<span data-ttu-id="94e11-141">Veri kutusu kenarı/ağ geçidi cihazında güncelleştirmeleri tarar.</span><span class="sxs-lookup"><span data-stu-id="94e11-141">Scans for updates on a data box edge/gateway device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeScanForUpdateByResourceIdParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e11-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="94e11-142">-Confirm</span></span>
<span data-ttu-id="94e11-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="94e11-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94e11-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94e11-144">-WhatIf</span></span>
<span data-ttu-id="94e11-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="94e11-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94e11-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="94e11-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94e11-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e11-147">CommonParameters</span></span>
<span data-ttu-id="94e11-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94e11-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e11-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="94e11-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e11-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94e11-150">INPUTS</span></span>

### <span data-ttu-id="94e11-151">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="94e11-151">None</span></span>

## <span data-ttu-id="94e11-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94e11-152">OUTPUTS</span></span>

### <span data-ttu-id="94e11-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="94e11-153">System.Boolean</span></span>

## <span data-ttu-id="94e11-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94e11-154">NOTES</span></span>

## <span data-ttu-id="94e11-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94e11-155">RELATED LINKS</span></span>
