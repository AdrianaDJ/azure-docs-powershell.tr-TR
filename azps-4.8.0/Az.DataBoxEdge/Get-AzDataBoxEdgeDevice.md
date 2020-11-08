---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 314ebb4412b88e5476a63cf5a1025f26e2c41e69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275056"
---
# <span data-ttu-id="cf435-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="cf435-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="cf435-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf435-102">SYNOPSIS</span></span>
<span data-ttu-id="cf435-103">Kullanılabilir veri kutusu uç cihazlarındaki bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="cf435-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="cf435-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf435-104">SYNTAX</span></span>

### <span data-ttu-id="cf435-105">ListByParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cf435-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf435-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="cf435-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf435-107">Geistdedinfobyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="cf435-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf435-108">Getnetworksettingbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="cf435-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf435-109">Getsummaryupdatebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="cf435-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf435-110">Getalertbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="cf435-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf435-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf435-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf435-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf435-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf435-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf435-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf435-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf435-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf435-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf435-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf435-116">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf435-116">DESCRIPTION</span></span>
<span data-ttu-id="cf435-117">**Get-AzDataBoxEdgeDevice** cmdlet 'ı kullanılabilir veri kutusu uç aygıtları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="cf435-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="cf435-118">Belirli bir cihazda bilgileri almak için kaynak grubu adıyla birlikte aygıtın adını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cf435-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="cf435-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf435-119">EXAMPLES</span></span>

### <span data-ttu-id="cf435-120">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cf435-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="cf435-121">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cf435-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="cf435-122">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="cf435-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="cf435-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf435-123">PARAMETERS</span></span>

### <span data-ttu-id="cf435-124">-Uyarı</span><span class="sxs-lookup"><span data-stu-id="cf435-124">-Alert</span></span>
<span data-ttu-id="cf435-125">Veri kutusu kenarı/ağ geçidi cihazında uyarıları getirme</span><span class="sxs-lookup"><span data-stu-id="cf435-125">Fetch the alerts on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAlertByResourceIdParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf435-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf435-126">-DefaultProfile</span></span>
<span data-ttu-id="cf435-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cf435-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf435-128">-Extendeınfo</span><span class="sxs-lookup"><span data-stu-id="cf435-128">-ExtendedInfo</span></span>
<span data-ttu-id="cf435-129">Belirtilen veri kutusu kenarı/veri kutusu ağ geçidi cihazı için ek bilgi alır</span><span class="sxs-lookup"><span data-stu-id="cf435-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetExtendedInfoByResourceIdParameterSet, GetExtendedInfoParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf435-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="cf435-130">-Name</span></span>
<span data-ttu-id="cf435-131">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="cf435-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf435-132">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="cf435-132">-NetworkSetting</span></span>
<span data-ttu-id="cf435-133">Belirtilen veri kutusunun uç/veri kutusu ağ geçidi aygıtının ağ ayarlarını alır</span><span class="sxs-lookup"><span data-stu-id="cf435-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNetworkSettingByResourceIdParameterSet, GetNetworkSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf435-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf435-134">-ResourceGroupName</span></span>
<span data-ttu-id="cf435-135">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="cf435-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf435-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cf435-136">-ResourceId</span></span>
<span data-ttu-id="cf435-137">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cf435-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet, GetExtendedInfoByResourceIdParameterSet, GetNetworkSettingByResourceIdParameterSet, GetSummaryUpdateByResourceIdParameterSet, GetAlertByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf435-138">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="cf435-138">-UpdateSummary</span></span>
<span data-ttu-id="cf435-139">Cihazın son taramasını temel alarak güncelleştirmelerin kullanılabilirliği hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="cf435-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="cf435-140">Ayrıca, cihazda devam eden indirme ve yükleme işleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="cf435-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetSummaryUpdateByResourceIdParameterSet, GetSummaryUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf435-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf435-141">CommonParameters</span></span>
<span data-ttu-id="cf435-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf435-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf435-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cf435-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf435-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf435-144">INPUTS</span></span>

### <span data-ttu-id="cf435-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cf435-145">None</span></span>

## <span data-ttu-id="cf435-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf435-146">OUTPUTS</span></span>

### <span data-ttu-id="cf435-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="cf435-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="cf435-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="cf435-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="cf435-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaboxedgedeviceextendeınfo</span><span class="sxs-lookup"><span data-stu-id="cf435-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="cf435-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="cf435-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="cf435-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="cf435-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="cf435-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf435-152">NOTES</span></span>

## <span data-ttu-id="cf435-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf435-153">RELATED LINKS</span></span>
