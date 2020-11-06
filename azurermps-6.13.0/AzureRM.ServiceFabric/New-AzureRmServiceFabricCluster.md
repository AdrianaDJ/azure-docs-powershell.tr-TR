---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/new-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 87fb451028fb0e345bd8748573424cf33066e52b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593651"
---
# <span data-ttu-id="1b4f8-101">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="1b4f8-101">New-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="1b4f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b4f8-102">SYNOPSIS</span></span>
<span data-ttu-id="1b4f8-103">Bu komut, yeni bir hizmet yapısı kümesi ayarlamak için sağladığınız sertifikaları veya sistem tarafından oluşturulan otomatik olarak imzalanan sertifikaları kullanır.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="1b4f8-104">Varsayılan bir şablonu veya sağladığınız özel bir şablonu kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="1b4f8-105">Otomatik olarak imzalanan sertifikaları dışarı aktarmak için bir klasör belirtme seçeneğiniz vardır ve bunları daha sonra anahtar kasasından alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b4f8-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b4f8-106">SYNTAX</span></span>

### <span data-ttu-id="1b4f8-107">ByDefaultArmTemplate (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1b4f8-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b4f8-108">Varexistingtuş Kasası</span><span class="sxs-lookup"><span data-stu-id="1b4f8-108">ByExistingKeyVault</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-VmPassword <SecureString>] -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b4f8-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="1b4f8-109">ByNewPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b4f8-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="1b4f8-110">ByExistingPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b4f8-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b4f8-111">DESCRIPTION</span></span>
<span data-ttu-id="1b4f8-112">**Yeni-AzureRmServiceFabricCluster** komutu, sağladığınız sertifikaları veya yeni bir hizmet yapısı kümesi ayarlamak için sistem tarafından oluşturulan otomatik olarak imzalanan sertifikaları kullanır.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-112">The **New-AzureRmServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="1b4f8-113">Kullanılan şablon, varsayılan bir şablon veya sağladığınız özel bir şablon olabilir.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="1b4f8-114">Kendinden imzalanan sertifikaları dışarı aktarmak için bir klasör belirtme veya bunları daha sonra anahtar kasasından getirmeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="1b4f8-115">Özel bir şablon ve parametre dosyası belirtiyorsanız, parametre dosyasında sertifika bilgilerini sağlamanız gerekmez, sistem bu parametreleri doldurur.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="1b4f8-116">Dört seçenek aşağıda ayrıntılıdır.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-116">The four options are detailed below.</span></span> <span data-ttu-id="1b4f8-117">Parametrelerin her biri için açıklamalar için aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="1b4f8-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b4f8-118">EXAMPLES</span></span>

### <span data-ttu-id="1b4f8-119">Örnek 1: kümeyi dağıtmak için yalnızca küme boyutunu, sertifika konu adını ve işletim sistemini belirtin.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="c:\certs"

Write-Output "Create cluster in '$clusterloc' with cert subject name '$subname' and cert output path '$pfxfolder'"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 5 -VmPassword $pass -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="1b4f8-120">Bu komut, kümeyi dağıtmak için yalnızca küme boyutunu, sertifika konu adını ve işletim sistemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="1b4f8-121">Örnek 2: bir anahtar kasada varolan bir sertifika kaynağını ve kümeyi dağıtmak için özel bir şablonu belirtme</span><span class="sxs-lookup"><span data-stu-id="1b4f8-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secretId
```

<span data-ttu-id="1b4f8-122">Bu komut, bir anahtar kasasına mevcut bir sertifika kaynağını ve kümeyi dağıtmak için özel bir şablonu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="1b4f8-123">Örnek 3: özel şablon kullanarak yeni küme oluşturma.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="1b4f8-124">Anahtar Kasası için farklı bir kaynak grubu adı belirtme ve sistemin bu sertifikaya yeni sertifika yüklemesini sağlamak</span><span class="sxs-lookup"><span data-stu-id="1b4f8-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.$clusterloc.cloudapp.azure.com" -f $RGName, $clusterloc
$pfxfolder="~\Documents"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="1b4f8-125">Bu komut özel bir şablon kullanarak yeni bir küme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="1b4f8-126">Anahtar Kasası için farklı bir kaynak grubu adı belirtme ve sistemin bu sertifikaya yeni sertifika yüklemesini sağlamak</span><span class="sxs-lookup"><span data-stu-id="1b4f8-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="1b4f8-127">Örnek 4: kendi sertifikanızı ve özel şablonunuzu getirin ve yeni bir küme oluşturun</span><span class="sxs-lookup"><span data-stu-id="1b4f8-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateFile $pfxsourcefile -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="1b4f8-128">Bu komut, kendi sertifikanızı ve özel şablonunuzu eklemenize ve yeni bir küme oluşturmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="1b4f8-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b4f8-129">PARAMETERS</span></span>

### <span data-ttu-id="1b4f8-130">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="1b4f8-130">-CertificateFile</span></span>
<span data-ttu-id="1b4f8-131">Birincil küme sertifikasının mevcut sertifika dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-131">The existing certificate file path for the primary cluster certificate.</span></span>

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

### <span data-ttu-id="1b4f8-132">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="1b4f8-132">-CertificateOutputFolder</span></span>
<span data-ttu-id="1b4f8-133">Oluşturulacak yeni sertifika dosyasının klasörü.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-133">The folder of the new certificate file to be created.</span></span>

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

### <span data-ttu-id="1b4f8-134">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="1b4f8-134">-CertificatePassword</span></span>
<span data-ttu-id="1b4f8-135">Sertifika dosyasının parolası.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-135">The password of the certificate file.</span></span>

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

### <span data-ttu-id="1b4f8-136">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="1b4f8-136">-CertificateSubjectName</span></span>
<span data-ttu-id="1b4f8-137">Oluşturulacak sertifikanın konu adı.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-137">The subject name of the certificate to be created.</span></span>

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

### <span data-ttu-id="1b4f8-138">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="1b4f8-138">-ClusterSize</span></span>
<span data-ttu-id="1b4f8-139">Kümedeki düğümlerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-139">The number of nodes in the cluster.</span></span> <span data-ttu-id="1b4f8-140">Varsayılan 5 düğümlerdir.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-140">Default are 5 nodes.</span></span>

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

### <span data-ttu-id="1b4f8-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b4f8-141">-DefaultProfile</span></span>
<span data-ttu-id="1b4f8-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b4f8-143">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="1b4f8-143">-KeyVaultName</span></span>
<span data-ttu-id="1b4f8-144">Azure Key kasa adı.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-144">Azure key vault name.</span></span> <span data-ttu-id="1b4f8-145">Verilmezse, kaynak grubu adına varsayılan olarak alınır.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-145">If not given, it will be defaulted to the resource group name.</span></span>

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

### <span data-ttu-id="1b4f8-146">-Keyvaultbalanucegroupname</span><span class="sxs-lookup"><span data-stu-id="1b4f8-146">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="1b4f8-147">Azure Key kasa kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-147">Azure key vault resource group name.</span></span> <span data-ttu-id="1b4f8-148">Verilmezse, kaynak grup adına varsayılan olarak alınır.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-148">If not given, it will be defaulted to resource group name.</span></span>

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

### <span data-ttu-id="1b4f8-149">-Konum</span><span class="sxs-lookup"><span data-stu-id="1b4f8-149">-Location</span></span>
<span data-ttu-id="1b4f8-150">Kaynak grubu konumu.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-150">The resource group location.</span></span>

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

### <span data-ttu-id="1b4f8-151">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b4f8-151">-Name</span></span>
<span data-ttu-id="1b4f8-152">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-152">Specify the name of the cluster.</span></span> <span data-ttu-id="1b4f8-153">Verilmezse, kaynak grubu adıyla aynı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-153">If not given, it will be same as resource group name.</span></span>

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

### <span data-ttu-id="1b4f8-154">-İşletim sistemi</span><span class="sxs-lookup"><span data-stu-id="1b4f8-154">-OS</span></span>
<span data-ttu-id="1b4f8-155">Kümeyi oluşturan VM 'lerin Işletim sistemi.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-155">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="1b4f8-156">-Parameterfıle</span><span class="sxs-lookup"><span data-stu-id="1b4f8-156">-ParameterFile</span></span>
<span data-ttu-id="1b4f8-157">Şablon parametre dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-157">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="1b4f8-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b4f8-158">-ResourceGroupName</span></span>
<span data-ttu-id="1b4f8-159">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-159">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1b4f8-160">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="1b4f8-160">-SecondaryCertificateFile</span></span>
<span data-ttu-id="1b4f8-161">İkincil küme sertifikasının mevcut sertifika dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-161">The existing certificate file path for the secondary cluster certificate.</span></span>

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

### <span data-ttu-id="1b4f8-162">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="1b4f8-162">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="1b4f8-163">Sertifika dosyasının parolası.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-163">The password of the certificate file.</span></span>

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

### <span data-ttu-id="1b4f8-164">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="1b4f8-164">-SecretIdentifier</span></span>
<span data-ttu-id="1b4f8-165">Var olan Azure Key kasa gizli URL 'SI; örneğin: ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-165">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

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

### <span data-ttu-id="1b4f8-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="1b4f8-166">-TemplateFile</span></span>
<span data-ttu-id="1b4f8-167">Şablon dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-167">The path to the template file.</span></span>

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

### <span data-ttu-id="1b4f8-168">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="1b4f8-168">-VmPassword</span></span>
<span data-ttu-id="1b4f8-169">VM 'nin parolası.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-169">The password of the Vm.</span></span>

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

### <span data-ttu-id="1b4f8-170">-VmSku</span><span class="sxs-lookup"><span data-stu-id="1b4f8-170">-VmSku</span></span>
<span data-ttu-id="1b4f8-171">VM SKU 'Su.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-171">The Vm Sku.</span></span>

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

### <span data-ttu-id="1b4f8-172">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="1b4f8-172">-VmUserName</span></span>
<span data-ttu-id="1b4f8-173">VM 'ye günlük Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-173">The user name for logging to Vm.</span></span>

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

### <span data-ttu-id="1b4f8-174">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b4f8-174">-Confirm</span></span>
<span data-ttu-id="1b4f8-175">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b4f8-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b4f8-176">-WhatIf</span></span>
<span data-ttu-id="1b4f8-177">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-177">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b4f8-178">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b4f8-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b4f8-179">CommonParameters</span></span>
<span data-ttu-id="1b4f8-180">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b4f8-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b4f8-181">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b4f8-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b4f8-182">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b4f8-182">INPUTS</span></span>

### <span data-ttu-id="1b4f8-183">System. String</span><span class="sxs-lookup"><span data-stu-id="1b4f8-183">System.String</span></span>
<span data-ttu-id="1b4f8-184">Parametreler: SertifikaDosyası (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), KeyVaultName (ByValue), Keyvaulteucegroupname (ByValue), yer (ByValue), ad (Bydeğeri), parametredeğeri (ByValue), SecondaryCertificateFile (ByValue),</span><span class="sxs-lookup"><span data-stu-id="1b4f8-184">Parameters: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), KeyVaultName (ByValue), KeyVaultResouceGroupName (ByValue), Location (ByValue), Name (ByValue), ParameterFile (ByValue), SecondaryCertificateFile (ByValue), SecretIdentifier (ByValue), TemplateFile (ByValue), VmUserName (ByValue)</span></span>

### <span data-ttu-id="1b4f8-185">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="1b4f8-185">System.Security.SecureString</span></span>
<span data-ttu-id="1b4f8-186">Parametreler: Sertifikaparolası (ByValue), SecondaryCertificatePassword (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1b4f8-186">Parameters: CertificatePassword (ByValue), SecondaryCertificatePassword (ByValue)</span></span>

### <span data-ttu-id="1b4f8-187">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1b4f8-187">System.Int32</span></span>
<span data-ttu-id="1b4f8-188">Parametreler: Kümeboyutu (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1b4f8-188">Parameters: ClusterSize (ByValue)</span></span>

### <span data-ttu-id="1b4f8-189">Microsoft. Azure. Commands. ServiceFabric. modeller. OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="1b4f8-189">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="1b4f8-190">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b4f8-190">OUTPUTS</span></span>

### <span data-ttu-id="1b4f8-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="1b4f8-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="1b4f8-192">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b4f8-192">NOTES</span></span>

## <span data-ttu-id="1b4f8-193">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b4f8-193">RELATED LINKS</span></span>
