---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: 9e5ba2d2ee228da30a887c0c7b318dd9d270d763
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110275"
---
# <span data-ttu-id="68ab2-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="68ab2-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="68ab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68ab2-102">SYNOPSIS</span></span>

<span data-ttu-id="68ab2-103">Bu komut, yeni bir hizmet yapısı kümesi ayarlamak için sağladığınız sertifikaları veya sistem tarafından oluşturulan otomatik olarak imzalanan sertifikaları kullanır.</span><span class="sxs-lookup"><span data-stu-id="68ab2-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="68ab2-104">Varsayılan bir şablonu veya sağladığınız özel bir şablonu kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="68ab2-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="68ab2-105">Otomatik olarak imzalanan sertifikaları dışarı aktarmak için bir klasör belirtme seçeneğiniz vardır ve bunları daha sonra anahtar kasasından alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68ab2-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

## <span data-ttu-id="68ab2-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68ab2-106">SYNTAX</span></span>

### <span data-ttu-id="68ab2-107">ByDefaultArmTemplate (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="68ab2-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68ab2-108">Varexistingtuş Kasası</span><span class="sxs-lookup"><span data-stu-id="68ab2-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-Thumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68ab2-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="68ab2-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68ab2-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="68ab2-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68ab2-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="68ab2-111">DESCRIPTION</span></span>

<span data-ttu-id="68ab2-112">**New-AzServiceFabricCluster** komutu, sağladığınız sertifikaları veya yeni bir hizmet yapısı kümesi ayarlamak için sistem tarafından oluşturulan otomatik olarak imzalanan sertifikaları kullanır.</span><span class="sxs-lookup"><span data-stu-id="68ab2-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="68ab2-113">Kullanılan şablon, varsayılan bir şablon veya sağladığınız özel bir şablon olabilir.</span><span class="sxs-lookup"><span data-stu-id="68ab2-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="68ab2-114">Kendinden imzalanan sertifikaları dışarı aktarmak için bir klasör belirtme veya bunları daha sonra anahtar kasasından getirmeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68ab2-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="68ab2-115">Özel bir şablon ve parametre dosyası belirtiyorsanız, parametre dosyasında sertifika bilgilerini sağlamanız gerekmez, sistem bu parametreleri doldurur.</span><span class="sxs-lookup"><span data-stu-id="68ab2-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="68ab2-116">Dört seçenek aşağıda ayrıntılıdır.</span><span class="sxs-lookup"><span data-stu-id="68ab2-116">The four options are detailed below.</span></span> <span data-ttu-id="68ab2-117">Parametrelerin her biri için açıklamalar için aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="68ab2-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="68ab2-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68ab2-118">EXAMPLES</span></span>

### <span data-ttu-id="68ab2-119">Örnek 1: kümeyi dağıtmak için yalnızca küme boyutunu, sertifika konu adını ve işletim sistemini belirtin</span><span class="sxs-lookup"><span data-stu-id="68ab2-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -f $resourceGroupName, $azureRegion
$localCertificateFolder = "c:\certs"

Write-Output "Create cluster in '$azureRegion' with cert subject name '$clusterDnsName' and cert output path '$localCertificateFolder'"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -Location $azureRegion -ClusterSize 5 -VmPassword $password -CertificateSubjectName $clusterDnsName -CertificateOutputFolder $localCertificateFolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="68ab2-120">Bu komut, kümeyi dağıtmak için yalnızca küme boyutunu, sertifika konu adını ve işletim sistemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="68ab2-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="68ab2-121">Örnek 2: bir anahtar kasada varolan bir sertifika kaynağını ve kümeyi dağıtmak için özel bir şablonu belirtme</span><span class="sxs-lookup"><span data-stu-id="68ab2-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>

```powershell
$resourceGroupName = "test20"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId = "https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -SecretIdentifier $secretId
```

<span data-ttu-id="68ab2-122">Bu komut, bir anahtar kasasına mevcut bir sertifika kaynağını ve kümeyi dağıtmak için özel bir şablonu belirtir.</span><span class="sxs-lookup"><span data-stu-id="68ab2-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="68ab2-123">Örnek 3: özel şablon kullanarak yeni küme oluşturma.</span><span class="sxs-lookup"><span data-stu-id="68ab2-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="68ab2-124">Anahtar Kasası için farklı bir kaynak grubu adı belirtme ve sistemin bu sertifikaya yeni sertifika yüklemesini sağlamak</span><span class="sxs-lookup"><span data-stu-id="68ab2-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$keyVaultResourceGroupName = " quickstart-kv-group"
$keyVaultName = "quickstart-kv"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -F $resourceGroupName, $azureRegion
$localCertificateFolder = "~\Documents"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateOutputFolder $localCertificateFolder -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName  -KeyVaultName $keyVaultName -CertificateSubjectName $clusterDnsName
```

<span data-ttu-id="68ab2-125">Bu komut özel bir şablon kullanarak yeni bir küme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="68ab2-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="68ab2-126">Anahtar Kasası için farklı bir kaynak grubu adı belirtme ve sistemin bu sertifikaya yeni sertifika yüklemesini sağlamak</span><span class="sxs-lookup"><span data-stu-id="68ab2-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="68ab2-127">Örnek 4: kendi sertifikanızı ve özel şablonunuzu getirin ve yeni bir küme oluşturun</span><span class="sxs-lookup"><span data-stu-id="68ab2-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "test20"
$keyVaultResourceGroupName = "test20kvrg"
$keyVaultName = "test20kv"
$localCertificateFile = "c:\Mycertificates\my2017Prodcert.pfx"
$templateParameterFile = "~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateFile $localCertificateFile -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName -KeyVaultName $keyVaultName
```

<span data-ttu-id="68ab2-128">Bu komut, kendi sertifikanızı ve özel şablonunuzu eklemenize ve yeni bir küme oluşturmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="68ab2-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="68ab2-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68ab2-129">PARAMETERS</span></span>

### <span data-ttu-id="68ab2-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="68ab2-130">-CertificateCommonName</span></span>

<span data-ttu-id="68ab2-131">Sertifika ortak adı</span><span class="sxs-lookup"><span data-stu-id="68ab2-131">Certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertCommonName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="68ab2-132">-CertificateFile</span></span>

<span data-ttu-id="68ab2-133">Birincil küme sertifikasının mevcut sertifika dosyası yolu</span><span class="sxs-lookup"><span data-stu-id="68ab2-133">The existing certificate file path for the primary cluster certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-134">-Certificateıssuerparmak Izi</span><span class="sxs-lookup"><span data-stu-id="68ab2-134">-CertificateIssuerThumbprint</span></span>

<span data-ttu-id="68ab2-135">Birden çok sayıda virgül ile ayrılmış sertifika veren parmak izi</span><span class="sxs-lookup"><span data-stu-id="68ab2-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertIssuerThumbprint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="68ab2-136">-CertificateOutputFolder</span></span>

<span data-ttu-id="68ab2-137">Oluşturulacak yeni sertifika dosyasının klasörü</span><span class="sxs-lookup"><span data-stu-id="68ab2-137">The folder of the new certificate file to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="68ab2-138">-CertificatePassword</span></span>

<span data-ttu-id="68ab2-139">Sertifika dosyasının parolası</span><span class="sxs-lookup"><span data-stu-id="68ab2-139">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="68ab2-140">-CertificateSubjectName</span></span>

<span data-ttu-id="68ab2-141">Oluşturulacak sertifikanın konu adı</span><span class="sxs-lookup"><span data-stu-id="68ab2-141">The subject name of the certificate to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Subject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="68ab2-142">-ClusterSize</span></span>

<span data-ttu-id="68ab2-143">Kümedeki düğümlerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="68ab2-143">The number of nodes in the cluster.</span></span>
<span data-ttu-id="68ab2-144">Varsayılan 5 düğümlerdir</span><span class="sxs-lookup"><span data-stu-id="68ab2-144">Default are 5 nodes</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ab2-145">-DefaultProfile</span></span>

<span data-ttu-id="68ab2-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="68ab2-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68ab2-147">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="68ab2-147">-KeyVaultName</span></span>

<span data-ttu-id="68ab2-148">Azure Anahtar Kasası adı verilmezse, kaynak grubu adına varsayılan olarak alınır</span><span class="sxs-lookup"><span data-stu-id="68ab2-148">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-149">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ab2-149">-KeyVaultResourceGroupName</span></span>

<span data-ttu-id="68ab2-150">Verilmezse Azure Anahtar Kasası kaynak grubu adı, kaynak grubu adına varsayılan olarak alınır</span><span class="sxs-lookup"><span data-stu-id="68ab2-150">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-151">-Konum</span><span class="sxs-lookup"><span data-stu-id="68ab2-151">-Location</span></span>

<span data-ttu-id="68ab2-152">Kaynak grubu konumu</span><span class="sxs-lookup"><span data-stu-id="68ab2-152">The resource group location</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-153">-Ad</span><span class="sxs-lookup"><span data-stu-id="68ab2-153">-Name</span></span>

<span data-ttu-id="68ab2-154">Yoksa, kümenin adını belirtin; verilmezse, kaynak grubu adı ile aynı olur</span><span class="sxs-lookup"><span data-stu-id="68ab2-154">Specify the name of the cluster, if not given it will be same as resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: ClusterName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-155">-İşletim sistemi</span><span class="sxs-lookup"><span data-stu-id="68ab2-155">-OS</span></span>

<span data-ttu-id="68ab2-156">Kümeyi oluşturan VM 'lerin Işletim sistemi.</span><span class="sxs-lookup"><span data-stu-id="68ab2-156">The Operating System of the VMs that make up the cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem
Parameter Sets: ByDefaultArmTemplate
Aliases: VmImage
Accepted values: WindowsServer2012R2Datacenter, WindowsServer2016Datacenter, WindowsServer2016DatacenterwithContainers, UbuntuServer1604

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-157">-Parameterfıle</span><span class="sxs-lookup"><span data-stu-id="68ab2-157">-ParameterFile</span></span>

<span data-ttu-id="68ab2-158">Şablon parametre dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="68ab2-158">The path to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ab2-159">-ResourceGroupName</span></span>

<span data-ttu-id="68ab2-160">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="68ab2-160">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="68ab2-161">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="68ab2-161">-SecondaryCertificateFile</span></span>

<span data-ttu-id="68ab2-162">İkincil küme sertifikasının mevcut sertifika dosyası yolu</span><span class="sxs-lookup"><span data-stu-id="68ab2-162">The existing certificate file path for the secondary cluster certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecSource

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-163">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="68ab2-163">-SecondaryCertificatePassword</span></span>

<span data-ttu-id="68ab2-164">Sertifika dosyasının parolası</span><span class="sxs-lookup"><span data-stu-id="68ab2-164">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecCertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-165">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="68ab2-165">-SecretIdentifier</span></span>

<span data-ttu-id="68ab2-166">Var olan Azure Key kasa gizli URL 'SI; örneğin ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="68ab2-166">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="68ab2-167">-TemplateFile</span></span>

<span data-ttu-id="68ab2-168">Şablon dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="68ab2-168">The path to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-169">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="68ab2-169">-Thumbprint</span></span>
<span data-ttu-id="68ab2-170">Sertifikanın parmak izi SecretIdentifier 'a daha fazla.</span><span class="sxs-lookup"><span data-stu-id="68ab2-170">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="68ab2-171">Anahtar Kasası yalnızca sertifika gizli olarak saklanabileceği ve cmdlet 'in parmak izini doğrulayamadığından, bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="68ab2-171">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-172">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="68ab2-172">-VmPassword</span></span>

<span data-ttu-id="68ab2-173">VM 'nin parolası.</span><span class="sxs-lookup"><span data-stu-id="68ab2-173">The password of the Vm.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-174">-VmSku</span><span class="sxs-lookup"><span data-stu-id="68ab2-174">-VmSku</span></span>

<span data-ttu-id="68ab2-175">VM SKU 'Su</span><span class="sxs-lookup"><span data-stu-id="68ab2-175">The Vm Sku</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: Sku

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-176">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="68ab2-176">-VmUserName</span></span>

<span data-ttu-id="68ab2-177">VM 'ye oturum açmak için Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="68ab2-177">The user name for logging to Vm</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ab2-178">-Onay</span><span class="sxs-lookup"><span data-stu-id="68ab2-178">-Confirm</span></span>

<span data-ttu-id="68ab2-179">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="68ab2-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68ab2-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68ab2-180">-WhatIf</span></span>

<span data-ttu-id="68ab2-181">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="68ab2-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68ab2-182">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="68ab2-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68ab2-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ab2-183">CommonParameters</span></span>
<span data-ttu-id="68ab2-184">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68ab2-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ab2-185">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="68ab2-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ab2-186">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68ab2-186">INPUTS</span></span>

### <span data-ttu-id="68ab2-187">System. String</span><span class="sxs-lookup"><span data-stu-id="68ab2-187">System.String</span></span>

### <span data-ttu-id="68ab2-188">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="68ab2-188">System.Security.SecureString</span></span>

### <span data-ttu-id="68ab2-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="68ab2-189">System.Int32</span></span>

### <span data-ttu-id="68ab2-190">Microsoft. Azure. Commands. ServiceFabric. modeller. OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="68ab2-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="68ab2-191">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68ab2-191">OUTPUTS</span></span>

### <span data-ttu-id="68ab2-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="68ab2-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="68ab2-193">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68ab2-193">NOTES</span></span>

## <span data-ttu-id="68ab2-194">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68ab2-194">RELATED LINKS</span></span>
