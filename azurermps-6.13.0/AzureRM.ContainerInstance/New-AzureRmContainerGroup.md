---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/new-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 1823759b72bdb3162164068732f3a8201fcfb589
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587252"
---
# <span data-ttu-id="afa74-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="afa74-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="afa74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afa74-102">SYNOPSIS</span></span>
<span data-ttu-id="afa74-103">Kapsayıcı grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="afa74-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afa74-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="afa74-104">SYNTAX</span></span>

### <span data-ttu-id="afa74-105">CreateContainerGroupBaseParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="afa74-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa74-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="afa74-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afa74-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="afa74-107">DESCRIPTION</span></span>
<span data-ttu-id="afa74-108">**Yeni-AzureRmContainerGroup** cmdlet 'leri bir kapsayıcı grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="afa74-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="afa74-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="afa74-109">EXAMPLES</span></span>

### <span data-ttu-id="afa74-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="afa74-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

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

<span data-ttu-id="afa74-111">Bu komut, en son Nginx görüntüsünü kullanan bir kapsayıcı grubu oluşturur ve bağlantı noktası 8000 ' i açan genel bir IP adresi ister.</span><span class="sxs-lookup"><span data-stu-id="afa74-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="afa74-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="afa74-112">Example 2</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

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

<span data-ttu-id="afa74-113">Bu komut kapsayıcı grubu oluşturur ve kapsayıcı içinde özel bir komut dosyası çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="afa74-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="afa74-114">Örnek 3: bir çalışma-tamamlanma kapsayıcısı grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="afa74-114">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

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

<span data-ttu-id="afa74-115">Bu komut, ' Merhaba ' ve durduran bir kapsayıcı grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="afa74-115">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="afa74-116">Örnek 4: Azure kapsayıcısı kayıt defterinde resim kullanarak kapsayıcı grubu oluşturur</span><span class="sxs-lookup"><span data-stu-id="afa74-116">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

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

<span data-ttu-id="afa74-117">Bu komut, Azure kapsayıcısı kayıt defterinde nginx görüntüsü kullanarak bir kapsayıcı grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="afa74-117">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="afa74-118">Örnek 5: özel kapsayıcı görüntüsü kayıt defterinde resim kullanarak kapsayıcı grubu oluşturur</span><span class="sxs-lookup"><span data-stu-id="afa74-118">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

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

<span data-ttu-id="afa74-119">Bu komut özel bir kapsayıcı görüntüsü kayıt defterinden özel bir resim kullanarak kapsayıcı grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="afa74-119">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="afa74-120">Örnek 6: Azure dosya birimini barındıran bir kapsayıcı grubu oluşturur</span><span class="sxs-lookup"><span data-stu-id="afa74-120">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountKey $mycred -AzureFileVolumeMountPath /mnt/azfile

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

<span data-ttu-id="afa74-121">Bu komut, sağlanan Azure dosya paylaşımını bağlayan bir kapsayıcı grubu oluşturur `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="afa74-121">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

## <span data-ttu-id="afa74-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="afa74-122">PARAMETERS</span></span>

### <span data-ttu-id="afa74-123">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="afa74-123">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="afa74-124">Ad alanının depolama hesabı adı olduğu ve anahtarın depolama hesabı anahtarı olduğu yerde takılacak Azure dosya paylaşımının depolama hesabı kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="afa74-124">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa74-125">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="afa74-125">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="afa74-126">Azure dosya birimi için bağlama yolu.</span><span class="sxs-lookup"><span data-stu-id="afa74-126">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa74-127">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="afa74-127">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="afa74-128">Takılacak Azure dosya paylaşımının adı.</span><span class="sxs-lookup"><span data-stu-id="afa74-128">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa74-129">-Komut</span><span class="sxs-lookup"><span data-stu-id="afa74-129">-Command</span></span>
<span data-ttu-id="afa74-130">Kapsayıcıda çalışan komut.</span><span class="sxs-lookup"><span data-stu-id="afa74-130">The command to run in the container.</span></span>

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

### <span data-ttu-id="afa74-131">-CPU</span><span class="sxs-lookup"><span data-stu-id="afa74-131">-Cpu</span></span>
<span data-ttu-id="afa74-132">Gerekli CPU çekirdeği.</span><span class="sxs-lookup"><span data-stu-id="afa74-132">The required CPU cores.</span></span>
<span data-ttu-id="afa74-133">Varsayılan: 1</span><span class="sxs-lookup"><span data-stu-id="afa74-133">Default: 1</span></span>

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

### <span data-ttu-id="afa74-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afa74-134">-DefaultProfile</span></span>
<span data-ttu-id="afa74-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="afa74-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa74-136">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="afa74-136">-DnsNameLabel</span></span>
<span data-ttu-id="afa74-137">IP adresi için DNS adı etiketi.</span><span class="sxs-lookup"><span data-stu-id="afa74-137">The DNS name label for the IP address.</span></span>

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

### <span data-ttu-id="afa74-138">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="afa74-138">-EnvironmentVariable</span></span>
<span data-ttu-id="afa74-139">Kapsayıcı ortam değişkenleri.</span><span class="sxs-lookup"><span data-stu-id="afa74-139">The container environment variables.</span></span>

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

### <span data-ttu-id="afa74-140">-Image</span><span class="sxs-lookup"><span data-stu-id="afa74-140">-Image</span></span>
<span data-ttu-id="afa74-141">Kapsayıcı görüntü.</span><span class="sxs-lookup"><span data-stu-id="afa74-141">The container image.</span></span>

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

### <span data-ttu-id="afa74-142">-Ipadresstype</span><span class="sxs-lookup"><span data-stu-id="afa74-142">-IpAddressType</span></span>
<span data-ttu-id="afa74-143">IP adresi türü.</span><span class="sxs-lookup"><span data-stu-id="afa74-143">The IP address type.</span></span>

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

### <span data-ttu-id="afa74-144">-Konum</span><span class="sxs-lookup"><span data-stu-id="afa74-144">-Location</span></span>
<span data-ttu-id="afa74-145">Kapsayıcı grubu konumu.</span><span class="sxs-lookup"><span data-stu-id="afa74-145">The container group Location.</span></span>
<span data-ttu-id="afa74-146">Kaynak grubunun konumu.</span><span class="sxs-lookup"><span data-stu-id="afa74-146">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="afa74-147">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="afa74-147">-MemoryInGB</span></span>
<span data-ttu-id="afa74-148">GB cinsinden gerekli bellek.</span><span class="sxs-lookup"><span data-stu-id="afa74-148">The required memory in GB.</span></span>
<span data-ttu-id="afa74-149">Varsayılan: 1,5</span><span class="sxs-lookup"><span data-stu-id="afa74-149">Default: 1.5</span></span>

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

### <span data-ttu-id="afa74-150">-Ad</span><span class="sxs-lookup"><span data-stu-id="afa74-150">-Name</span></span>
<span data-ttu-id="afa74-151">Kapsayıcı grubu adı.</span><span class="sxs-lookup"><span data-stu-id="afa74-151">The container group name.</span></span>

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

### <span data-ttu-id="afa74-152">-OsType</span><span class="sxs-lookup"><span data-stu-id="afa74-152">-OsType</span></span>
<span data-ttu-id="afa74-153">Kapsayıcı işletim sistemi türü.</span><span class="sxs-lookup"><span data-stu-id="afa74-153">The container OS type.</span></span>
<span data-ttu-id="afa74-154">Varsayılan: Linux</span><span class="sxs-lookup"><span data-stu-id="afa74-154">Default: Linux</span></span>

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

### <span data-ttu-id="afa74-155">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="afa74-155">-Port</span></span>
<span data-ttu-id="afa74-156">Açılacak bağlantı noktaları.</span><span class="sxs-lookup"><span data-stu-id="afa74-156">The port(s) to open.</span></span> <span data-ttu-id="afa74-157">Varsayılan: [80]</span><span class="sxs-lookup"><span data-stu-id="afa74-157">Default: [80]</span></span>

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

### <span data-ttu-id="afa74-158">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="afa74-158">-RegistryCredential</span></span>
<span data-ttu-id="afa74-159">Özel kapsayıcı kayıt defteri kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="afa74-159">The custom container registry credential.</span></span>

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

### <span data-ttu-id="afa74-160">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="afa74-160">-RegistryServerDomain</span></span>
<span data-ttu-id="afa74-161">Özel kapsayıcı kayıt defteri oturum açma sunucusu.</span><span class="sxs-lookup"><span data-stu-id="afa74-161">The custom container registry login server.</span></span>

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

### <span data-ttu-id="afa74-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afa74-162">-ResourceGroupName</span></span>
<span data-ttu-id="afa74-163">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="afa74-163">The resource group name.</span></span>

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

### <span data-ttu-id="afa74-164">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="afa74-164">-RestartPolicy</span></span>
<span data-ttu-id="afa74-165">Kapsayıcı yeniden başlatma ilkesi.</span><span class="sxs-lookup"><span data-stu-id="afa74-165">The container restart policy.</span></span> <span data-ttu-id="afa74-166">Varsayılan: her zaman</span><span class="sxs-lookup"><span data-stu-id="afa74-166">Default: Always</span></span>

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

### <span data-ttu-id="afa74-167">Etiketli</span><span class="sxs-lookup"><span data-stu-id="afa74-167">-Tag</span></span>
<span data-ttu-id="afa74-168">{{Etiket doldur açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="afa74-168">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="afa74-169">-Onay</span><span class="sxs-lookup"><span data-stu-id="afa74-169">-Confirm</span></span>
<span data-ttu-id="afa74-170">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="afa74-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afa74-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afa74-171">-WhatIf</span></span>
<span data-ttu-id="afa74-172">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="afa74-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afa74-173">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="afa74-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afa74-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afa74-174">CommonParameters</span></span>
<span data-ttu-id="afa74-175">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="afa74-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afa74-176">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afa74-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afa74-177">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="afa74-177">INPUTS</span></span>

### <span data-ttu-id="afa74-178">System. String</span><span class="sxs-lookup"><span data-stu-id="afa74-178">System.String</span></span>

### <span data-ttu-id="afa74-179">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="afa74-179">System.Collections.Hashtable</span></span>

## <span data-ttu-id="afa74-180">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="afa74-180">OUTPUTS</span></span>

### <span data-ttu-id="afa74-181">Microsoft. Azure. Commands. Containerınstance. modeller. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="afa74-181">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="afa74-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="afa74-182">NOTES</span></span>

## <span data-ttu-id="afa74-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="afa74-183">RELATED LINKS</span></span>
