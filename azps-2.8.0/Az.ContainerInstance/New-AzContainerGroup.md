---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/new-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
ms.openlocfilehash: 76719250ca7909d86d288b987b9598a58ab5fb88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752617"
---
# <span data-ttu-id="e6ece-101">New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="e6ece-101">New-AzContainerGroup</span></span>

## <span data-ttu-id="e6ece-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6ece-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ece-103">Kapsayıcı grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6ece-103">Creates a container group.</span></span>

## <span data-ttu-id="e6ece-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6ece-104">SYNTAX</span></span>

### <span data-ttu-id="e6ece-105">CreateContainerGroupBaseParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e6ece-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-AssignIdentity] [-OsType <String>]
 [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6ece-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="e6ece-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-AssignIdentity] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6ece-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span><span class="sxs-lookup"><span data-stu-id="e6ece-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6ece-108">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6ece-108">ExplicitIdentityParameterSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6ece-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6ece-109">DESCRIPTION</span></span>
<span data-ttu-id="e6ece-110">**Yeni-AzContainerGroup** cmdlet 'leri bir kapsayıcı grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6ece-110">The **New-AzContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="e6ece-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6ece-111">EXAMPLES</span></span>

### <span data-ttu-id="e6ece-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e6ece-112">Example 1</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="e6ece-113">Bu komut, en son Nginx görüntüsünü kullanan bir kapsayıcı grubu oluşturur ve bağlantı noktası 8000 ' i açan genel bir IP adresi ister.</span><span class="sxs-lookup"><span data-stu-id="e6ece-113">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="e6ece-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e6ece-114">Example 2</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="e6ece-115">Bu komut kapsayıcı grubu oluşturur ve kapsayıcı içinde özel bir komut dosyası çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="e6ece-115">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="e6ece-116">Örnek 3: bir çalışma-tamamlanma kapsayıcısı grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6ece-116">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="e6ece-117">Bu komut, ' Merhaba ' ve durduran bir kapsayıcı grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6ece-117">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="e6ece-118">Örnek 4: Azure kapsayıcısı kayıt defterinde resim kullanarak kapsayıcı grubu oluşturur</span><span class="sxs-lookup"><span data-stu-id="e6ece-118">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myacr}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="e6ece-119">Bu komut, Azure kapsayıcısı kayıt defterinde nginx görüntüsü kullanarak bir kapsayıcı grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6ece-119">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="e6ece-120">Örnek 5: özel kapsayıcı görüntüsü kayıt defterinde resim kullanarak kapsayıcı grubu oluşturur</span><span class="sxs-lookup"><span data-stu-id="e6ece-120">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="e6ece-121">Bu komut özel bir kapsayıcı görüntüsü kayıt defterinden özel bir resim kullanarak kapsayıcı grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6ece-121">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="e6ece-122">Örnek 6: Azure dosya birimini barındıran bir kapsayıcı grubu oluşturur</span><span class="sxs-lookup"><span data-stu-id="e6ece-122">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image alpine -AzFileVolumeShareName myshare -AzFileVolumeAccountKey $mycred -AzFileVolumeMountPath /mnt/azfile

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  : {AzureFile}
State                    : Running
Events                   : {}
```

<span data-ttu-id="e6ece-123">Bu komut, sağlanan Azure dosya paylaşımını bağlayan bir kapsayıcı grubu oluşturur `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="e6ece-123">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

### <span data-ttu-id="e6ece-124">Örnek 7</span><span class="sxs-lookup"><span data-stu-id="e6ece-124">Example 7</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -AssignIdentity

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="e6ece-125">Bu komutlar, en son Nginx görüntüsünü kullanarak sistem tarafından atanan kimlik ile bir kapsayıcı grubu oluşturur ve bağlantı noktası 8000 ' i açan genel bir IP adresi ister.</span><span class="sxs-lookup"><span data-stu-id="e6ece-125">This commands creates a container group with system assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="e6ece-126">Örnek 8</span><span class="sxs-lookup"><span data-stu-id="e6ece-126">Example 8</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -IdentityType SystemAssignedUserAssigned -IdentityId /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<UserIdentityName>

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="e6ece-127">Bu komutlar, en son Nginx görüntüsünü kullanarak sistem atanmış ve Kullanıcı tarafından atanmış bir kapsayıcı grubu oluşturur ve bağlantı noktası 8000 ' i açan genel bir IP adresi ister.</span><span class="sxs-lookup"><span data-stu-id="e6ece-127">This commands creates a container group with system assigned and user assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

## <span data-ttu-id="e6ece-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6ece-128">PARAMETERS</span></span>

### <span data-ttu-id="e6ece-129">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="e6ece-129">-AssignIdentity</span></span>
<span data-ttu-id="e6ece-130">Sistemin atadığı kimliği etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="e6ece-130">Enable system assigned identity</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateContainerGroupBaseParamSet, CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ece-131">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e6ece-131">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="e6ece-132">Ad alanının depolama hesabı adı olduğu ve anahtarın depolama hesabı anahtarı olduğu yerde takılacak Azure dosya paylaşımının depolama hesabı kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="e6ece-132">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ece-133">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="e6ece-133">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="e6ece-134">Azure dosya birimi için bağlama yolu.</span><span class="sxs-lookup"><span data-stu-id="e6ece-134">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ece-135">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="e6ece-135">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="e6ece-136">Takılacak Azure dosya paylaşımının adı.</span><span class="sxs-lookup"><span data-stu-id="e6ece-136">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ece-137">-Komut</span><span class="sxs-lookup"><span data-stu-id="e6ece-137">-Command</span></span>
<span data-ttu-id="e6ece-138">Kapsayıcıda çalışan komut.</span><span class="sxs-lookup"><span data-stu-id="e6ece-138">The command to run in the container.</span></span>

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

### <span data-ttu-id="e6ece-139">-CPU</span><span class="sxs-lookup"><span data-stu-id="e6ece-139">-Cpu</span></span>
<span data-ttu-id="e6ece-140">Gerekli CPU çekirdeği.</span><span class="sxs-lookup"><span data-stu-id="e6ece-140">The required CPU cores.</span></span>
<span data-ttu-id="e6ece-141">Varsayılan: 1</span><span class="sxs-lookup"><span data-stu-id="e6ece-141">Default: 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ece-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ece-142">-DefaultProfile</span></span>
<span data-ttu-id="e6ece-143">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e6ece-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6ece-144">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="e6ece-144">-DnsNameLabel</span></span>
<span data-ttu-id="e6ece-145">IP adresi için DNS adı etiketi.</span><span class="sxs-lookup"><span data-stu-id="e6ece-145">The DNS name label for the IP address.</span></span>

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

### <span data-ttu-id="e6ece-146">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="e6ece-146">-EnvironmentVariable</span></span>
<span data-ttu-id="e6ece-147">Kapsayıcı ortam değişkenleri.</span><span class="sxs-lookup"><span data-stu-id="e6ece-147">The container environment variables.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ece-148">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="e6ece-148">-IdentityId</span></span>
<span data-ttu-id="e6ece-149">Kullanıcının kimlik kimlikleri</span><span class="sxs-lookup"><span data-stu-id="e6ece-149">The user assigned identity IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ece-150">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e6ece-150">-IdentityType</span></span>
<span data-ttu-id="e6ece-151">Yönetilen kimlik türü</span><span class="sxs-lookup"><span data-stu-id="e6ece-151">The managed identity type</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerInstance.Models.ResourceIdentityType
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet, ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ece-152">-Image</span><span class="sxs-lookup"><span data-stu-id="e6ece-152">-Image</span></span>
<span data-ttu-id="e6ece-153">Kapsayıcı görüntü.</span><span class="sxs-lookup"><span data-stu-id="e6ece-153">The container image.</span></span>

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

### <span data-ttu-id="e6ece-154">-Ipadresstype</span><span class="sxs-lookup"><span data-stu-id="e6ece-154">-IpAddressType</span></span>
<span data-ttu-id="e6ece-155">IP adresi türü.</span><span class="sxs-lookup"><span data-stu-id="e6ece-155">The IP address type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Public

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ece-156">-Konum</span><span class="sxs-lookup"><span data-stu-id="e6ece-156">-Location</span></span>
<span data-ttu-id="e6ece-157">Kapsayıcı grubu konumu.</span><span class="sxs-lookup"><span data-stu-id="e6ece-157">The container group Location.</span></span>
<span data-ttu-id="e6ece-158">Kaynak grubunun konumu.</span><span class="sxs-lookup"><span data-stu-id="e6ece-158">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="e6ece-159">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="e6ece-159">-MemoryInGB</span></span>
<span data-ttu-id="e6ece-160">GB cinsinden gerekli bellek.</span><span class="sxs-lookup"><span data-stu-id="e6ece-160">The required memory in GB.</span></span>
<span data-ttu-id="e6ece-161">Varsayılan: 1,5</span><span class="sxs-lookup"><span data-stu-id="e6ece-161">Default: 1.5</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: Memory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ece-162">-Ad</span><span class="sxs-lookup"><span data-stu-id="e6ece-162">-Name</span></span>
<span data-ttu-id="e6ece-163">Kapsayıcı grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e6ece-163">The container group name.</span></span>

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

### <span data-ttu-id="e6ece-164">-OsType</span><span class="sxs-lookup"><span data-stu-id="e6ece-164">-OsType</span></span>
<span data-ttu-id="e6ece-165">Kapsayıcı işletim sistemi türü.</span><span class="sxs-lookup"><span data-stu-id="e6ece-165">The container OS type.</span></span>
<span data-ttu-id="e6ece-166">Varsayılan: Linux</span><span class="sxs-lookup"><span data-stu-id="e6ece-166">Default: Linux</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Linux, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ece-167">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="e6ece-167">-Port</span></span>
<span data-ttu-id="e6ece-168">Açılacak bağlantı noktaları.</span><span class="sxs-lookup"><span data-stu-id="e6ece-168">The port(s) to open.</span></span> <span data-ttu-id="e6ece-169">Varsayılan: [80]</span><span class="sxs-lookup"><span data-stu-id="e6ece-169">Default: [80]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ece-170">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="e6ece-170">-RegistryCredential</span></span>
<span data-ttu-id="e6ece-171">Özel kapsayıcı kayıt defteri kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="e6ece-171">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ece-172">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="e6ece-172">-RegistryServerDomain</span></span>
<span data-ttu-id="e6ece-173">Özel kapsayıcı kayıt defteri oturum açma sunucusu.</span><span class="sxs-lookup"><span data-stu-id="e6ece-173">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ece-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6ece-174">-ResourceGroupName</span></span>
<span data-ttu-id="e6ece-175">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e6ece-175">The resource group name.</span></span>

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

### <span data-ttu-id="e6ece-176">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="e6ece-176">-RestartPolicy</span></span>
<span data-ttu-id="e6ece-177">Kapsayıcı yeniden başlatma ilkesi.</span><span class="sxs-lookup"><span data-stu-id="e6ece-177">The container restart policy.</span></span> <span data-ttu-id="e6ece-178">Varsayılan: her zaman</span><span class="sxs-lookup"><span data-stu-id="e6ece-178">Default: Always</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Always, Never, OnFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ece-179">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e6ece-179">-Tag</span></span>
<span data-ttu-id="e6ece-180">{{Etiket doldur açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="e6ece-180">{{Fill Tag Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ece-181">-Onay</span><span class="sxs-lookup"><span data-stu-id="e6ece-181">-Confirm</span></span>
<span data-ttu-id="e6ece-182">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e6ece-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6ece-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6ece-183">-WhatIf</span></span>
<span data-ttu-id="e6ece-184">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6ece-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6ece-185">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e6ece-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6ece-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ece-186">CommonParameters</span></span>
<span data-ttu-id="e6ece-187">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6ece-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ece-188">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6ece-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ece-189">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6ece-189">INPUTS</span></span>

### <span data-ttu-id="e6ece-190">System. String</span><span class="sxs-lookup"><span data-stu-id="e6ece-190">System.String</span></span>

### <span data-ttu-id="e6ece-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="e6ece-191">System.String[]</span></span>

### <span data-ttu-id="e6ece-192">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e6ece-192">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e6ece-193">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6ece-193">OUTPUTS</span></span>

### <span data-ttu-id="e6ece-194">Microsoft. Azure. Commands. Containerınstance. modeller. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="e6ece-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="e6ece-195">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6ece-195">NOTES</span></span>

## <span data-ttu-id="e6ece-196">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6ece-196">RELATED LINKS</span></span>
