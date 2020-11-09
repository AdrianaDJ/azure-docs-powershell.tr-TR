---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
ms.openlocfilehash: f2244bc1d0471924ad7f69ff600e70e92fdc809a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324205"
---
# <span data-ttu-id="1af97-101">New-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="1af97-101">New-AzStackEdgeRole</span></span>

## <span data-ttu-id="1af97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1af97-102">SYNOPSIS</span></span>
<span data-ttu-id="1af97-103">Cihaz için yeni bir rol oluşturur</span><span class="sxs-lookup"><span data-stu-id="1af97-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="1af97-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1af97-104">SYNTAX</span></span>

### <span data-ttu-id="1af97-105">ConnectionStringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1af97-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> [-RoleStatus <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1af97-106">Iotparameterset</span><span class="sxs-lookup"><span data-stu-id="1af97-106">IotParameterSet</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 [-RoleStatus <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1af97-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1af97-107">DESCRIPTION</span></span>
<span data-ttu-id="1af97-108">**New-AzStackEdgeRole** cmdlet 'ı yığın uç aygıtı için yeni bir rol oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1af97-108">The **New-AzStackEdgeRole** cmdlet creates a new Role for a Stack Edge device.</span></span>

## <span data-ttu-id="1af97-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1af97-109">EXAMPLES</span></span>

### <span data-ttu-id="1af97-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1af97-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="1af97-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1af97-111">PARAMETERS</span></span>

### <span data-ttu-id="1af97-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="1af97-112">-AsJob</span></span>
<span data-ttu-id="1af97-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1af97-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1af97-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1af97-114">-ConnectionString</span></span>
<span data-ttu-id="1af97-115">Bağlantı dizelerini sağlamak için</span><span class="sxs-lookup"><span data-stu-id="1af97-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="1af97-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af97-116">-DefaultProfile</span></span>
<span data-ttu-id="1af97-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1af97-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1af97-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="1af97-118">-DeviceName</span></span>
<span data-ttu-id="1af97-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="1af97-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af97-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="1af97-120">-DeviceProperty</span></span>
<span data-ttu-id="1af97-121">Cihaz özelliklerini sağlamak için</span><span class="sxs-lookup"><span data-stu-id="1af97-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="1af97-122">-Şifrelemetuşu</span><span class="sxs-lookup"><span data-stu-id="1af97-122">-EncryptionKey</span></span>
<span data-ttu-id="1af97-123">Edge aygıtının şifreleme anahtarı</span><span class="sxs-lookup"><span data-stu-id="1af97-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="1af97-124">-Iotdeviceaccesskey</span><span class="sxs-lookup"><span data-stu-id="1af97-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="1af97-125">IoT cihazı erişim anahtarı</span><span class="sxs-lookup"><span data-stu-id="1af97-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="1af97-126">-Iotdeviceconnectionstring</span><span class="sxs-lookup"><span data-stu-id="1af97-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="1af97-127">Lütfen ıOT cihazı bağlantı dizesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="1af97-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="1af97-128">-Iotdeviceıd</span><span class="sxs-lookup"><span data-stu-id="1af97-128">-IotDeviceId</span></span>
<span data-ttu-id="1af97-129">IoT aygıtının cihaz kimliği</span><span class="sxs-lookup"><span data-stu-id="1af97-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="1af97-130">-Iotedgedeviceaccesskey</span><span class="sxs-lookup"><span data-stu-id="1af97-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="1af97-131">IoT Edge aygıtının erişim anahtarı</span><span class="sxs-lookup"><span data-stu-id="1af97-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="1af97-132">-Iotedgedeviceconnectionstring</span><span class="sxs-lookup"><span data-stu-id="1af97-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="1af97-133">Lütfen sınır aygıtının bağlantı dizesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="1af97-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="1af97-134">-Iotedgedeviceıd</span><span class="sxs-lookup"><span data-stu-id="1af97-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="1af97-135">IoT Edge aygıtının kimliği</span><span class="sxs-lookup"><span data-stu-id="1af97-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="1af97-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="1af97-136">-IotHostHub</span></span>
<span data-ttu-id="1af97-137">Hosthub adresi</span><span class="sxs-lookup"><span data-stu-id="1af97-137">Hosthub address</span></span>

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

### <span data-ttu-id="1af97-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="1af97-138">-Name</span></span>
<span data-ttu-id="1af97-139">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="1af97-139">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af97-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="1af97-140">-Platform</span></span>
<span data-ttu-id="1af97-141">Ex: Linux için platformu sağlama</span><span class="sxs-lookup"><span data-stu-id="1af97-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="1af97-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af97-142">-ResourceGroupName</span></span>
<span data-ttu-id="1af97-143">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="1af97-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af97-144">-Roldurumu</span><span class="sxs-lookup"><span data-stu-id="1af97-144">-RoleStatus</span></span>
<span data-ttu-id="1af97-145">Durumu etkinleştirme/devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="1af97-145">Provide the status enable/disable</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af97-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="1af97-146">-Confirm</span></span>
<span data-ttu-id="1af97-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1af97-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1af97-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1af97-148">-WhatIf</span></span>
<span data-ttu-id="1af97-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1af97-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1af97-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1af97-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1af97-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af97-151">CommonParameters</span></span>
<span data-ttu-id="1af97-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1af97-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af97-153">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1af97-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af97-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1af97-154">INPUTS</span></span>

### <span data-ttu-id="1af97-155">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1af97-155">None</span></span>

## <span data-ttu-id="1af97-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1af97-156">OUTPUTS</span></span>

### <span data-ttu-id="1af97-157">Microsoft. Azure. PowerShell. cmdlet. StackEdge. model. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="1af97-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="1af97-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1af97-158">NOTES</span></span>

## <span data-ttu-id="1af97-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1af97-159">RELATED LINKS</span></span>
