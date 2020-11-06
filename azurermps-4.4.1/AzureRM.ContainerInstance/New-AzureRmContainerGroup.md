---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 63c54c5f1bb17af82e353b70e757bf91b1208958
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593160"
---
# <span data-ttu-id="5bdab-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="5bdab-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="5bdab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bdab-102">SYNOPSIS</span></span>
<span data-ttu-id="5bdab-103">Kapsayıcı grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5bdab-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bdab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5bdab-104">SYNTAX</span></span>

### <span data-ttu-id="5bdab-105">CreateContainerGroupBaseParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5bdab-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bdab-106">CreateContainerGroupWithRegistryParamSet</span><span class="sxs-lookup"><span data-stu-id="5bdab-106">CreateContainerGroupWithRegistryParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>]
 -RegistryCredential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bdab-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5bdab-107">DESCRIPTION</span></span>
<span data-ttu-id="5bdab-108">**Yeni-AzureRmContainerGroup** cmdlet 'leri bir kapsayıcı grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5bdab-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="5bdab-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5bdab-109">EXAMPLES</span></span>

### <span data-ttu-id="5bdab-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5bdab-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port 8000

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
```

<span data-ttu-id="5bdab-111">Bu komut, en son Nginx görüntüsünü kullanan bir kapsayıcı grubu oluşturur ve bağlantı noktası 8000 ' i açan genel bir IP adresi ister.</span><span class="sxs-lookup"><span data-stu-id="5bdab-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="5bdab-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5bdab-112">Example 2</span></span>
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
```

<span data-ttu-id="5bdab-113">Bu komut kapsayıcı grubu oluşturur ve kapsayıcı içinde özel bir komut dosyası çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="5bdab-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="5bdab-114">Örnek 3: Azure kapsayıcısı kayıt defterinde resim kullanarak kapsayıcı grubu oluşturur</span><span class="sxs-lookup"><span data-stu-id="5bdab-114">Example 3: Creates a container group using image in Azure Container Registry</span></span>
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
```

<span data-ttu-id="5bdab-115">Bu komut, Azure kapsayıcısı kayıt defterinde nginx görüntüsü kullanarak bir kapsayıcı grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5bdab-115">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="5bdab-116">Örnek 4: özel kapsayıcı görüntüsü kayıt defterinde resim kullanarak kapsayıcı grubu oluşturur</span><span class="sxs-lookup"><span data-stu-id="5bdab-116">Example 4: Creates a container group using image in custom container image registry</span></span>
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
```

<span data-ttu-id="5bdab-117">Bu komut özel bir kapsayıcı görüntüsü kayıt defterinden özel bir resim kullanarak kapsayıcı grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5bdab-117">This commands creates a container group using a custom image from a custom container image registry.</span></span>

## <span data-ttu-id="5bdab-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5bdab-118">PARAMETERS</span></span>

### <span data-ttu-id="5bdab-119">-Komut</span><span class="sxs-lookup"><span data-stu-id="5bdab-119">-Command</span></span>
<span data-ttu-id="5bdab-120">Kapsayıcıda çalışan komut.</span><span class="sxs-lookup"><span data-stu-id="5bdab-120">The command to run in the container.</span></span>

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

### <span data-ttu-id="5bdab-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="5bdab-121">-Confirm</span></span>
<span data-ttu-id="5bdab-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5bdab-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bdab-123">-CPU</span><span class="sxs-lookup"><span data-stu-id="5bdab-123">-Cpu</span></span>
<span data-ttu-id="5bdab-124">Gerekli CPU çekirdeği.</span><span class="sxs-lookup"><span data-stu-id="5bdab-124">The required CPU cores.</span></span>
<span data-ttu-id="5bdab-125">Varsayılan: 1</span><span class="sxs-lookup"><span data-stu-id="5bdab-125">Default: 1</span></span>

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

### <span data-ttu-id="5bdab-126">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="5bdab-126">-EnvironmentVariable</span></span>
<span data-ttu-id="5bdab-127">Kapsayıcı ortam değişkenleri.</span><span class="sxs-lookup"><span data-stu-id="5bdab-127">The container environment variables.</span></span>

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

### <span data-ttu-id="5bdab-128">-Image</span><span class="sxs-lookup"><span data-stu-id="5bdab-128">-Image</span></span>
<span data-ttu-id="5bdab-129">Kapsayıcı görüntü.</span><span class="sxs-lookup"><span data-stu-id="5bdab-129">The container image.</span></span>

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

### <span data-ttu-id="5bdab-130">-Ipadresstype</span><span class="sxs-lookup"><span data-stu-id="5bdab-130">-IpAddressType</span></span>
<span data-ttu-id="5bdab-131">IP adresi türü.</span><span class="sxs-lookup"><span data-stu-id="5bdab-131">The IP address type.</span></span>

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

### <span data-ttu-id="5bdab-132">-Konum</span><span class="sxs-lookup"><span data-stu-id="5bdab-132">-Location</span></span>
<span data-ttu-id="5bdab-133">Kapsayıcı grubu konumu.</span><span class="sxs-lookup"><span data-stu-id="5bdab-133">The container group Location.</span></span>
<span data-ttu-id="5bdab-134">Kaynak grubunun konumu.</span><span class="sxs-lookup"><span data-stu-id="5bdab-134">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="5bdab-135">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="5bdab-135">-MemoryInGB</span></span>
<span data-ttu-id="5bdab-136">GB cinsinden gerekli bellek.</span><span class="sxs-lookup"><span data-stu-id="5bdab-136">The required memory in GB.</span></span>
<span data-ttu-id="5bdab-137">Varsayılan: 1,5</span><span class="sxs-lookup"><span data-stu-id="5bdab-137">Default: 1.5</span></span>

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

### <span data-ttu-id="5bdab-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="5bdab-138">-Name</span></span>
<span data-ttu-id="5bdab-139">Kapsayıcı grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5bdab-139">The container group name.</span></span>

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

### <span data-ttu-id="5bdab-140">-OsType</span><span class="sxs-lookup"><span data-stu-id="5bdab-140">-OsType</span></span>
<span data-ttu-id="5bdab-141">Kapsayıcı işletim sistemi türü.</span><span class="sxs-lookup"><span data-stu-id="5bdab-141">The container OS type.</span></span>
<span data-ttu-id="5bdab-142">Varsayılan: Linux</span><span class="sxs-lookup"><span data-stu-id="5bdab-142">Default: Linux</span></span>

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

### <span data-ttu-id="5bdab-143">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="5bdab-143">-Port</span></span>
<span data-ttu-id="5bdab-144">Açılacak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="5bdab-144">The port to open.</span></span>
<span data-ttu-id="5bdab-145">Varsayılan: 80</span><span class="sxs-lookup"><span data-stu-id="5bdab-145">Default: 80</span></span>

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

### <span data-ttu-id="5bdab-146">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="5bdab-146">-RegistryCredential</span></span>
<span data-ttu-id="5bdab-147">Özel kapsayıcı kayıt defteri kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="5bdab-147">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdab-148">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="5bdab-148">-RegistryServerDomain</span></span>
<span data-ttu-id="5bdab-149">Özel kapsayıcı kayıt defteri oturum açma sunucusu.</span><span class="sxs-lookup"><span data-stu-id="5bdab-149">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdab-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bdab-150">-ResourceGroupName</span></span>
<span data-ttu-id="5bdab-151">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5bdab-151">The resource group name.</span></span>

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

### <span data-ttu-id="5bdab-152">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5bdab-152">-Tag</span></span>
<span data-ttu-id="5bdab-153">{{Etiket doldur açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="5bdab-153">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="5bdab-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bdab-154">-WhatIf</span></span>
<span data-ttu-id="5bdab-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5bdab-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bdab-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5bdab-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bdab-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bdab-157">-DefaultProfile</span></span>
<span data-ttu-id="5bdab-158">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5bdab-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bdab-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bdab-159">CommonParameters</span></span>
<span data-ttu-id="5bdab-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5bdab-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bdab-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bdab-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bdab-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5bdab-162">INPUTS</span></span>

### <span data-ttu-id="5bdab-163">System. String</span><span class="sxs-lookup"><span data-stu-id="5bdab-163">System.String</span></span>
<span data-ttu-id="5bdab-164">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5bdab-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5bdab-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5bdab-165">OUTPUTS</span></span>

### <span data-ttu-id="5bdab-166">Microsoft. Azure. Commands. Containerınstance. modeller. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="5bdab-166">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="5bdab-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5bdab-167">NOTES</span></span>

## <span data-ttu-id="5bdab-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5bdab-168">RELATED LINKS</span></span>

