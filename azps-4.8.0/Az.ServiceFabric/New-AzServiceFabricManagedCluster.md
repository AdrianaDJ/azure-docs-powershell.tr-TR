---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 9dd54f0f1ca56a8bedf3550e238a4308b519925d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267630"
---
# <span data-ttu-id="f0c27-101">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="f0c27-101">New-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="f0c27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0c27-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c27-103">Yeni yönetilen küme oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f0c27-103">Create new managed cluster.</span></span>

## <span data-ttu-id="f0c27-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0c27-104">SYNTAX</span></span>

### <span data-ttu-id="f0c27-105">ClientCertByTp (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f0c27-105">ClientCertByTp (Default)</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertThumbprint <String> -AdminPassword <SecureString> [-AdminUserName <String>]
 [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>] [-DnsName <String>]
 [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0c27-106">Istemciz CN</span><span class="sxs-lookup"><span data-stu-id="f0c27-106">ClientCertByCn</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertCommonName <String> [-ClientCertIssuerThumbprint <String[]>] -AdminPassword <SecureString>
 [-AdminUserName <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0c27-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0c27-107">DESCRIPTION</span></span>
<span data-ttu-id="f0c27-108">Bu cmdlet, düğüm türleri olmadan yönetilen bir küme kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f0c27-108">This cmdlet will create a managed cluster resource without node types.</span></span> <span data-ttu-id="f0c27-109">Kümeye birincil düğüm türü eklemek için [Yeni-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md)kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0c27-109">To bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span></span>

## <span data-ttu-id="f0c27-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0c27-110">EXAMPLES</span></span>

### <span data-ttu-id="f0c27-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f0c27-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -AdminPassword $password -Verbose
```

<span data-ttu-id="f0c27-112">Bu komut, varsayılan temel SKU ile küme kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f0c27-112">This command creates a cluster resource with default basic sku.</span></span>

### <span data-ttu-id="f0c27-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f0c27-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -ClientCertThumbprint XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -ClientCertIsAdmin -AdminPassword $password -Sku Standard -Verbose
```

<span data-ttu-id="f0c27-114">Bu komut, bir ilk yönetici istemci sertifikası ve standart SKU ile merkezileştirme için bir küme kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f0c27-114">This command creates a cluster resource in centraluseuap with an initial admin client certificate and standard sku.</span></span>

## <span data-ttu-id="f0c27-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0c27-115">PARAMETERS</span></span>

### <span data-ttu-id="f0c27-116">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="f0c27-116">-AdminPassword</span></span>
<span data-ttu-id="f0c27-117">Sanal makinelerde kullanılan yönetici parolası.</span><span class="sxs-lookup"><span data-stu-id="f0c27-117">Admin password used for the virtual machines.</span></span>

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

### <span data-ttu-id="f0c27-118">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="f0c27-118">-AdminUserName</span></span>
<span data-ttu-id="f0c27-119">Sanal makinelerde kullanılan yönetici parolası.</span><span class="sxs-lookup"><span data-stu-id="f0c27-119">Admin password used for the virtual machines.</span></span>
<span data-ttu-id="f0c27-120">Varsayılan: vmadmin.</span><span class="sxs-lookup"><span data-stu-id="f0c27-120">Default: vmadmin.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "vmadmin"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c27-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="f0c27-121">-AsJob</span></span>
<span data-ttu-id="f0c27-122">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="f0c27-122">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f0c27-123">-ClientCertCommonName</span><span class="sxs-lookup"><span data-stu-id="f0c27-123">-ClientCertCommonName</span></span>
<span data-ttu-id="f0c27-124">İstemci sertifikası ortak adı.</span><span class="sxs-lookup"><span data-stu-id="f0c27-124">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c27-125">-ClientCertIsAdmin</span><span class="sxs-lookup"><span data-stu-id="f0c27-125">-ClientCertIsAdmin</span></span>
<span data-ttu-id="f0c27-126">İstemci sertifikasının yönetici düzeyine sahip olup olmadığını belirtmek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0c27-126">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="f0c27-127">-Clientcertissuerparmak Izi</span><span class="sxs-lookup"><span data-stu-id="f0c27-127">-ClientCertIssuerThumbprint</span></span>
<span data-ttu-id="f0c27-128">İstemci sertifikası için veren parmak izleri listesi.</span><span class="sxs-lookup"><span data-stu-id="f0c27-128">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="f0c27-129">Yalnızca ClientCertCommonName ile birlikte kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0c27-129">Only use in combination with ClientCertCommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c27-130">-Clientcertparmak Izi</span><span class="sxs-lookup"><span data-stu-id="f0c27-130">-ClientCertThumbprint</span></span>
<span data-ttu-id="f0c27-131">İstemci sertifikası parmak izi.</span><span class="sxs-lookup"><span data-stu-id="f0c27-131">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c27-132">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="f0c27-132">-ClientConnectionPort</span></span>
<span data-ttu-id="f0c27-133">Kümeye yönelik istemci bağlantılarında kullanılan bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="f0c27-133">Port used for client connections to the cluster.</span></span>
<span data-ttu-id="f0c27-134">Varsayılan: 19000.</span><span class="sxs-lookup"><span data-stu-id="f0c27-134">Default: 19000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c27-135">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="f0c27-135">-CodeVersion</span></span>
<span data-ttu-id="f0c27-136">Küme hizmeti doku kodu sürümü.</span><span class="sxs-lookup"><span data-stu-id="f0c27-136">Cluster service fabric code version.</span></span>
<span data-ttu-id="f0c27-137">Yalnızca yükseltme modu El Ile olduğunda kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0c27-137">Only use if upgrade mode is Manual.</span></span>

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

### <span data-ttu-id="f0c27-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c27-138">-DefaultProfile</span></span>
<span data-ttu-id="f0c27-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0c27-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0c27-140">-DnsName</span><span class="sxs-lookup"><span data-stu-id="f0c27-140">-DnsName</span></span>
<span data-ttu-id="f0c27-141">Kümenin DNS adı.</span><span class="sxs-lookup"><span data-stu-id="f0c27-141">Cluster's dns name.</span></span>

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

### <span data-ttu-id="f0c27-142">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="f0c27-142">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="f0c27-143">Kümenin http bağlantılarında kullanılan bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="f0c27-143">Port used for http connections to the cluster.</span></span>
<span data-ttu-id="f0c27-144">Varsayılan: 19080.</span><span class="sxs-lookup"><span data-stu-id="f0c27-144">Default: 19080.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19080
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c27-145">-Konum</span><span class="sxs-lookup"><span data-stu-id="f0c27-145">-Location</span></span>
<span data-ttu-id="f0c27-146">Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="f0c27-146">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c27-147">-Ad</span><span class="sxs-lookup"><span data-stu-id="f0c27-147">-Name</span></span>
<span data-ttu-id="f0c27-148">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="f0c27-148">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c27-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0c27-149">-ResourceGroupName</span></span>
<span data-ttu-id="f0c27-150">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="f0c27-150">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="f0c27-151">-Smarproxyenvseçpointport</span><span class="sxs-lookup"><span data-stu-id="f0c27-151">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="f0c27-152">Uç ara sunucu</span><span class="sxs-lookup"><span data-stu-id="f0c27-152">Endpoint used by reverse proxy.</span></span>

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

### <span data-ttu-id="f0c27-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="f0c27-153">-Sku</span></span>
<span data-ttu-id="f0c27-154">Kümenin SKU 'Su, Seçenekler temel: en az 3 tohum düğümüne sahip olacak ve yalnızca 1 düğüm türüne ve Standard 'a izin verir: en az 5 tohum düğümüne sahip olur ve birden çok düğüm türüne izin verir.</span><span class="sxs-lookup"><span data-stu-id="f0c27-154">Cluster's Sku, the options are Basic: it will have a minimum of 3 seed nodes and only allows 1 node type and Standard: it will have a minimum of 5 seed nodes and allows multiple node types.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ManagedClusterSku
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: Basic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c27-155">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="f0c27-155">-UpgradeMode</span></span>
<span data-ttu-id="f0c27-156">Küme hizmeti doku kodu sürüm yükseltme modu.</span><span class="sxs-lookup"><span data-stu-id="f0c27-156">Cluster service fabric code version upgrade mode.</span></span>
<span data-ttu-id="f0c27-157">Otomatik veya el Ile.</span><span class="sxs-lookup"><span data-stu-id="f0c27-157">Automatic or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c27-158">-Usetestexgeri</span><span class="sxs-lookup"><span data-stu-id="f0c27-158">-UseTestExtension</span></span>
<span data-ttu-id="f0c27-159">Kümenin, hizmet testi VMSS Uzantısı ile öne dolacaktır.</span><span class="sxs-lookup"><span data-stu-id="f0c27-159">If Specify The cluster will be crated with service test vmss extension.</span></span>

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

### <span data-ttu-id="f0c27-160">-Onay</span><span class="sxs-lookup"><span data-stu-id="f0c27-160">-Confirm</span></span>
<span data-ttu-id="f0c27-161">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f0c27-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0c27-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0c27-162">-WhatIf</span></span>
<span data-ttu-id="f0c27-163">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f0c27-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0c27-164">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f0c27-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0c27-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c27-165">CommonParameters</span></span>
<span data-ttu-id="f0c27-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0c27-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c27-167">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f0c27-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c27-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0c27-168">INPUTS</span></span>

### <span data-ttu-id="f0c27-169">System. String</span><span class="sxs-lookup"><span data-stu-id="f0c27-169">System.String</span></span>

## <span data-ttu-id="f0c27-170">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0c27-170">OUTPUTS</span></span>

### <span data-ttu-id="f0c27-171">Microsoft. Azure. Commands. ServiceFabric. modeller. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="f0c27-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="f0c27-172">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0c27-172">NOTES</span></span>

## <span data-ttu-id="f0c27-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0c27-173">RELATED LINKS</span></span>

[<span data-ttu-id="f0c27-174">Yeni-Azhizmetifabricmanagednodetype</span><span class="sxs-lookup"><span data-stu-id="f0c27-174">New-AzServiceFabricManagedNodeType</span></span>](./New-AzServiceFabricManagedNodeType.md)