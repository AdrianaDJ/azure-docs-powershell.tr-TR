---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
ms.openlocfilehash: f25aeb501ff046a25330ad5db47bbdb06fbe7b35
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096523"
---
# <span data-ttu-id="d3a96-101">Invoke-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d3a96-101">Invoke-AzStackEdgeDevice</span></span>

## <span data-ttu-id="d3a96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a96-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a96-103">Cihazda belirli eylemleri başlatır.</span><span class="sxs-lookup"><span data-stu-id="d3a96-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="d3a96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3a96-104">SYNTAX</span></span>

### <span data-ttu-id="d3a96-105">InvokeScanForUpdateParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d3a96-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3a96-106">Invokefetchupdatesbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d3a96-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3a96-107">Invokeınstallupdatesbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d3a96-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3a96-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3a96-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3a96-109">Invokeınstallupdateparameterset</span><span class="sxs-lookup"><span data-stu-id="d3a96-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3a96-110">Invokefetchupdateparameterset</span><span class="sxs-lookup"><span data-stu-id="d3a96-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3a96-111">Invokefetchupdatesbydeviceobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="d3a96-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3a96-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3a96-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3a96-113">Invokeınstallupdatesbydeviceobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="d3a96-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3a96-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3a96-114">DESCRIPTION</span></span>
<span data-ttu-id="d3a96-115">**Invoke-AzStackEdgeDevice** cmdlet 'ı yığın uç aygıtında güncelleştirmeleri taramak, indirmek ve yüklemek için eylemleri çağırır.</span><span class="sxs-lookup"><span data-stu-id="d3a96-115">The **Invoke-AzStackEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Stack Edge device.</span></span> <span data-ttu-id="d3a96-116">Otomatik tarama cihazda günlük olarak çalışır, bu cmdlet 'i çalıştırarak taramayı açıkça tetikleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d3a96-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="d3a96-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3a96-117">EXAMPLES</span></span>

### <span data-ttu-id="d3a96-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d3a96-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="d3a96-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d3a96-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="d3a96-120">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="d3a96-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="d3a96-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3a96-121">PARAMETERS</span></span>

### <span data-ttu-id="d3a96-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="d3a96-122">-AsJob</span></span>
<span data-ttu-id="d3a96-123">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d3a96-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3a96-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a96-124">-DefaultProfile</span></span>
<span data-ttu-id="d3a96-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3a96-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3a96-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="d3a96-126">-DeviceObject</span></span>
<span data-ttu-id="d3a96-127">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="d3a96-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3a96-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="d3a96-128">-FetchUpdate</span></span>
<span data-ttu-id="d3a96-129">Yığın Edge/ağ geçidi cihazında güncelleştirmeleri indirir</span><span class="sxs-lookup"><span data-stu-id="d3a96-129">Downloads the updates on a Stack edge/gateway device</span></span>

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

### <span data-ttu-id="d3a96-130">-Installupdate</span><span class="sxs-lookup"><span data-stu-id="d3a96-130">-InstallUpdate</span></span>
<span data-ttu-id="d3a96-131">, Güncelleştirmeleri yığın Edge/Gateway cihazında yükler</span><span class="sxs-lookup"><span data-stu-id="d3a96-131">Installs the updates on the Stack edge/gateway device</span></span>

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

### <span data-ttu-id="d3a96-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="d3a96-132">-Name</span></span>
<span data-ttu-id="d3a96-133">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="d3a96-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3a96-134">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d3a96-134">-PassThru</span></span>
<span data-ttu-id="d3a96-135">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="d3a96-135">returns true if successful</span></span>

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

### <span data-ttu-id="d3a96-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a96-136">-ResourceGroupName</span></span>
<span data-ttu-id="d3a96-137">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d3a96-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3a96-138">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d3a96-138">-ResourceId</span></span>
<span data-ttu-id="d3a96-139">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d3a96-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3a96-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="d3a96-140">-ScanForUpdate</span></span>
<span data-ttu-id="d3a96-141">Yığın Edge/ağ geçidi cihazında güncelleştirmeleri tarar.</span><span class="sxs-lookup"><span data-stu-id="d3a96-141">Scans for updates on a Stack edge/gateway device.</span></span>

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

### <span data-ttu-id="d3a96-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="d3a96-142">-Confirm</span></span>
<span data-ttu-id="d3a96-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d3a96-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3a96-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3a96-144">-WhatIf</span></span>
<span data-ttu-id="d3a96-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3a96-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3a96-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d3a96-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3a96-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a96-147">CommonParameters</span></span>
<span data-ttu-id="d3a96-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3a96-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a96-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d3a96-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a96-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3a96-150">INPUTS</span></span>

### <span data-ttu-id="d3a96-151">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d3a96-151">None</span></span>

## <span data-ttu-id="d3a96-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3a96-152">OUTPUTS</span></span>

### <span data-ttu-id="d3a96-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3a96-153">System.Boolean</span></span>

## <span data-ttu-id="d3a96-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3a96-154">NOTES</span></span>

## <span data-ttu-id="d3a96-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3a96-155">RELATED LINKS</span></span>
