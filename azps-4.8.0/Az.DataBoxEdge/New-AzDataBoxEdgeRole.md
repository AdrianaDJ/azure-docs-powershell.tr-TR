---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
ms.openlocfilehash: aa44399adcfd5e39d956215b7ca824e5ef9abd60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268030"
---
# <span data-ttu-id="3ca03-101">New-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3ca03-101">New-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="3ca03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ca03-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca03-103">Cihaz için yeni bir rol oluşturur</span><span class="sxs-lookup"><span data-stu-id="3ca03-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="3ca03-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ca03-104">SYNTAX</span></span>

### <span data-ttu-id="3ca03-105">ConnectionStringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3ca03-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> -RoleStatus <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca03-106">Iotparameterset</span><span class="sxs-lookup"><span data-stu-id="3ca03-106">IotParameterSet</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 -RoleStatus <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ca03-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ca03-107">DESCRIPTION</span></span>
<span data-ttu-id="3ca03-108">**New-AzDataBoxEdgeRole** cmdlet 'ı bir veri kutusu uç aygıtı için yeni bir rol oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ca03-108">The **New-AzDataBoxEdgeRole** cmdlet creates a new Role for a Data Box Edge device.</span></span>

## <span data-ttu-id="3ca03-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ca03-109">EXAMPLES</span></span>

### <span data-ttu-id="3ca03-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3ca03-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="3ca03-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ca03-111">PARAMETERS</span></span>

### <span data-ttu-id="3ca03-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="3ca03-112">-AsJob</span></span>
<span data-ttu-id="3ca03-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3ca03-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ca03-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="3ca03-114">-ConnectionString</span></span>
<span data-ttu-id="3ca03-115">Bağlantı dizelerini sağlamak için</span><span class="sxs-lookup"><span data-stu-id="3ca03-115">To Provide Connection Strings</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca03-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca03-116">-DefaultProfile</span></span>
<span data-ttu-id="3ca03-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3ca03-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ca03-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="3ca03-118">-DeviceName</span></span>
<span data-ttu-id="3ca03-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="3ca03-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca03-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="3ca03-120">-DeviceProperty</span></span>
<span data-ttu-id="3ca03-121">Cihaz özelliklerini sağlamak için</span><span class="sxs-lookup"><span data-stu-id="3ca03-121">To Provide Device Properties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IotParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca03-122">-Şifrelemetuşu</span><span class="sxs-lookup"><span data-stu-id="3ca03-122">-EncryptionKey</span></span>
<span data-ttu-id="3ca03-123">Edge aygıtının şifreleme anahtarı</span><span class="sxs-lookup"><span data-stu-id="3ca03-123">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca03-124">-Iotdeviceaccesskey</span><span class="sxs-lookup"><span data-stu-id="3ca03-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="3ca03-125">IoT cihazı erişim anahtarı</span><span class="sxs-lookup"><span data-stu-id="3ca03-125">Iot Device Access Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca03-126">-Iotdeviceconnectionstring</span><span class="sxs-lookup"><span data-stu-id="3ca03-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="3ca03-127">Lütfen ıOT cihazı bağlantı dizesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="3ca03-127">Please provide connection string of IOT Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca03-128">-Iotdeviceıd</span><span class="sxs-lookup"><span data-stu-id="3ca03-128">-IotDeviceId</span></span>
<span data-ttu-id="3ca03-129">IoT aygıtının cihaz kimliği</span><span class="sxs-lookup"><span data-stu-id="3ca03-129">Device Id of the Iot Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca03-130">-Iotedgedeviceaccesskey</span><span class="sxs-lookup"><span data-stu-id="3ca03-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="3ca03-131">IoT Edge aygıtının erişim anahtarı</span><span class="sxs-lookup"><span data-stu-id="3ca03-131">Access key of the Iot Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca03-132">-Iotedgedeviceconnectionstring</span><span class="sxs-lookup"><span data-stu-id="3ca03-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="3ca03-133">Lütfen sınır aygıtının bağlantı dizesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="3ca03-133">Please provide connection string of Edge Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca03-134">-Iotedgedeviceıd</span><span class="sxs-lookup"><span data-stu-id="3ca03-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="3ca03-135">IoT Edge aygıtının kimliği</span><span class="sxs-lookup"><span data-stu-id="3ca03-135">Id of the Iot Edge Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca03-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="3ca03-136">-IotHostHub</span></span>
<span data-ttu-id="3ca03-137">Hosthub adresi</span><span class="sxs-lookup"><span data-stu-id="3ca03-137">Hosthub address</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca03-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="3ca03-138">-Name</span></span>
<span data-ttu-id="3ca03-139">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="3ca03-139">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca03-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="3ca03-140">-Platform</span></span>
<span data-ttu-id="3ca03-141">Ex: Linux için platformu sağlama</span><span class="sxs-lookup"><span data-stu-id="3ca03-141">Provide the Platform, for ex: Linux</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca03-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca03-142">-ResourceGroupName</span></span>
<span data-ttu-id="3ca03-143">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="3ca03-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca03-144">-Roldurumu</span><span class="sxs-lookup"><span data-stu-id="3ca03-144">-RoleStatus</span></span>
<span data-ttu-id="3ca03-145">Durumu etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="3ca03-145">Provide the status enable/disable</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca03-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="3ca03-146">-Confirm</span></span>
<span data-ttu-id="3ca03-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3ca03-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ca03-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca03-148">-WhatIf</span></span>
<span data-ttu-id="3ca03-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3ca03-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ca03-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3ca03-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ca03-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca03-151">CommonParameters</span></span>
<span data-ttu-id="3ca03-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ca03-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca03-153">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3ca03-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca03-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ca03-154">INPUTS</span></span>

### <span data-ttu-id="3ca03-155">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3ca03-155">None</span></span>

## <span data-ttu-id="3ca03-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ca03-156">OUTPUTS</span></span>

### <span data-ttu-id="3ca03-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3ca03-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="3ca03-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ca03-158">NOTES</span></span>

## <span data-ttu-id="3ca03-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ca03-159">RELATED LINKS</span></span>
