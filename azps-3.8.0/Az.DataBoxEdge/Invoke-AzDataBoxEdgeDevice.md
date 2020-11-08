---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 29bf8cf612d3569480c62784466879095ebcdb6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098883"
---
# <span data-ttu-id="4c5b2-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="4c5b2-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="4c5b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c5b2-102">SYNOPSIS</span></span>
<span data-ttu-id="4c5b2-103">Cihazda belirli eylemleri başlatır.</span><span class="sxs-lookup"><span data-stu-id="4c5b2-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="4c5b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c5b2-104">SYNTAX</span></span>

### <span data-ttu-id="4c5b2-105">InvokeScanForUpdateParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4c5b2-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c5b2-106">Invokefetchupdatesbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4c5b2-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c5b2-107">Invokeınstallupdatesbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4c5b2-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c5b2-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c5b2-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c5b2-109">Invokeınstallupdateparameterset</span><span class="sxs-lookup"><span data-stu-id="4c5b2-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c5b2-110">Invokefetchupdateparameterset</span><span class="sxs-lookup"><span data-stu-id="4c5b2-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c5b2-111">Invokefetchupdatesbydeviceobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="4c5b2-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c5b2-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c5b2-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c5b2-113">Invokeınstallupdatesbydeviceobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="4c5b2-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c5b2-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c5b2-114">DESCRIPTION</span></span>
<span data-ttu-id="4c5b2-115">**Invoke-AzDataBoxEdgeDevice** cmdlet 'ı, veri kutusu Edge cihazında güncelleştirmeleri taramak, indirmek ve yüklemek için eylemleri çağırır.</span><span class="sxs-lookup"><span data-stu-id="4c5b2-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="4c5b2-116">Otomatik tarama cihazda günlük olarak çalışır, bu cmdlet 'i çalıştırarak taramayı açıkça tetikleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c5b2-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="4c5b2-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c5b2-117">EXAMPLES</span></span>

### <span data-ttu-id="4c5b2-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4c5b2-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="4c5b2-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4c5b2-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="4c5b2-120">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="4c5b2-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="4c5b2-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c5b2-121">PARAMETERS</span></span>

### <span data-ttu-id="4c5b2-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="4c5b2-122">-AsJob</span></span>
<span data-ttu-id="4c5b2-123">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4c5b2-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c5b2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c5b2-124">-DefaultProfile</span></span>
<span data-ttu-id="4c5b2-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c5b2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c5b2-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="4c5b2-126">-DeviceObject</span></span>
<span data-ttu-id="4c5b2-127">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="4c5b2-127">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="4c5b2-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="4c5b2-128">-FetchUpdate</span></span>
<span data-ttu-id="4c5b2-129">Veri kutusu kenarı/ağ geçidi cihazında güncelleştirmeleri indirir</span><span class="sxs-lookup"><span data-stu-id="4c5b2-129">Downloads the updates on a data box edge/gateway device</span></span>

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

### <span data-ttu-id="4c5b2-130">-Installupdate</span><span class="sxs-lookup"><span data-stu-id="4c5b2-130">-InstallUpdate</span></span>
<span data-ttu-id="4c5b2-131">Veri kutusu kenarı/ağ geçidi cihazında güncelleştirmeleri yükler</span><span class="sxs-lookup"><span data-stu-id="4c5b2-131">Installs the updates on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="4c5b2-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c5b2-132">-Name</span></span>
<span data-ttu-id="4c5b2-133">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="4c5b2-133">Device Name</span></span>

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

### <span data-ttu-id="4c5b2-134">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4c5b2-134">-PassThru</span></span>
<span data-ttu-id="4c5b2-135">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="4c5b2-135">returns true if successful</span></span>

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

### <span data-ttu-id="4c5b2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c5b2-136">-ResourceGroupName</span></span>
<span data-ttu-id="4c5b2-137">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4c5b2-137">Resource Group Name</span></span>

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

### <span data-ttu-id="4c5b2-138">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4c5b2-138">-ResourceId</span></span>
<span data-ttu-id="4c5b2-139">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4c5b2-139">Azure ResourceId</span></span>

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

### <span data-ttu-id="4c5b2-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="4c5b2-140">-ScanForUpdate</span></span>
<span data-ttu-id="4c5b2-141">Veri kutusu kenarı/ağ geçidi cihazında güncelleştirmeleri tarar.</span><span class="sxs-lookup"><span data-stu-id="4c5b2-141">Scans for updates on a data box edge/gateway device.</span></span>

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

### <span data-ttu-id="4c5b2-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="4c5b2-142">-Confirm</span></span>
<span data-ttu-id="4c5b2-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4c5b2-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c5b2-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c5b2-144">-WhatIf</span></span>
<span data-ttu-id="4c5b2-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c5b2-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c5b2-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4c5b2-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c5b2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c5b2-147">CommonParameters</span></span>
<span data-ttu-id="4c5b2-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c5b2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c5b2-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4c5b2-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c5b2-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c5b2-150">INPUTS</span></span>

### <span data-ttu-id="4c5b2-151">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4c5b2-151">None</span></span>

## <span data-ttu-id="4c5b2-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c5b2-152">OUTPUTS</span></span>

### <span data-ttu-id="4c5b2-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4c5b2-153">System.Boolean</span></span>

## <span data-ttu-id="4c5b2-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c5b2-154">NOTES</span></span>

## <span data-ttu-id="4c5b2-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c5b2-155">RELATED LINKS</span></span>
