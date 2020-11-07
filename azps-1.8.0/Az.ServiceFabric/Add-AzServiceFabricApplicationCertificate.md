---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
ms.openlocfilehash: 58547205bc0edae3ea1ab9ff56d3df1ef71214f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759126"
---
# <span data-ttu-id="be164-101">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="be164-101">Add-AzServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="be164-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be164-102">SYNOPSIS</span></span>
<span data-ttu-id="be164-103">Kümeyi oluşturan sanal makine ölçek kümesine yeni bir sertifika ekleyin.</span><span class="sxs-lookup"><span data-stu-id="be164-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="be164-104">Sertifika, uygulama sertifikası olarak kullanılmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="be164-104">The certificate is intended to be used as an application certificate.</span></span>

## <span data-ttu-id="be164-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be164-105">SYNTAX</span></span>

### <span data-ttu-id="be164-106">Varexistingtuş Kasası</span><span class="sxs-lookup"><span data-stu-id="be164-106">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be164-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="be164-107">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be164-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="be164-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be164-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="be164-109">DESCRIPTION</span></span>
<span data-ttu-id="be164-110">Kümedeki tüm düğümlere sertifika yüklemek için **Add-AzServiceFabricApplicationCertificate** kullanın.</span><span class="sxs-lookup"><span data-stu-id="be164-110">Use **Add-AzServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="be164-111">Zaten sahip olduğunuz bir sertifikayı belirtebilir ya da sistemin sizin için yeni bir sertifika üretmesine ve yeni veya mevcut bir Azure anahtar kasasına yüklemesini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="be164-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="be164-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be164-112">EXAMPLES</span></span>

### <span data-ttu-id="be164-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="be164-113">Example 1</span></span>
```
PS c:> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="be164-114">Bu komut, var olan Azure Key kasasından kümenin tüm düğüm türlerine sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="be164-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="be164-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="be164-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="be164-116">Bu komut, Azure Anahtar Kasası 'nda Anahtar Kasası kaynak grubu adı ve Anahtar Kasası adı olan kendinden imzalanan bir sertifika oluşturur, kümenin tüm düğüm türlerine yükler ve ' c:\Test ' klasörünün altında sertifikayı indirir.</span><span class="sxs-lookup"><span data-stu-id="be164-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="be164-117">İndirilen sertifikanın adı, Anahtar Kasası sertifikasının adıyla aynıdır.</span><span class="sxs-lookup"><span data-stu-id="be164-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="be164-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be164-118">PARAMETERS</span></span>

### <span data-ttu-id="be164-119">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="be164-119">-CertificateCommonName</span></span>
<span data-ttu-id="be164-120">Sertifika ortak adı</span><span class="sxs-lookup"><span data-stu-id="be164-120">Certificate common name</span></span>

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

### <span data-ttu-id="be164-121">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="be164-121">-CertificateFile</span></span>
<span data-ttu-id="be164-122">Var olan sertifika dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="be164-122">The existing certificate file path.</span></span>

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

### <span data-ttu-id="be164-123">-Certificateıssuerparmak Izi</span><span class="sxs-lookup"><span data-stu-id="be164-123">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="be164-124">Birden çok sayıda virgül ile ayrılmış sertifika veren parmak izi</span><span class="sxs-lookup"><span data-stu-id="be164-124">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="be164-125">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="be164-125">-CertificateOutputFolder</span></span>
<span data-ttu-id="be164-126">Oluşturulacak yeni sertifikanın klasör yolu.</span><span class="sxs-lookup"><span data-stu-id="be164-126">The folder path of the new certificate to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be164-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="be164-127">-CertificatePassword</span></span>
<span data-ttu-id="be164-128">Pfx dosyasının parolası.</span><span class="sxs-lookup"><span data-stu-id="be164-128">The password of the pfx file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be164-129">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="be164-129">-CertificateSubjectName</span></span>
<span data-ttu-id="be164-130">Oluşturulacak sertifikanın DNS adı.</span><span class="sxs-lookup"><span data-stu-id="be164-130">The Dns name of the certificate to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Subject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be164-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be164-131">-DefaultProfile</span></span>
<span data-ttu-id="be164-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be164-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be164-133">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="be164-133">-KeyVaultName</span></span>
<span data-ttu-id="be164-134">Azure Key kasa adı.</span><span class="sxs-lookup"><span data-stu-id="be164-134">Azure key vault name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be164-135">-Keyvaultbalanucegroupname</span><span class="sxs-lookup"><span data-stu-id="be164-135">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="be164-136">Azure Key kasa kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="be164-136">Azure key vault resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be164-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="be164-137">-Name</span></span>
<span data-ttu-id="be164-138">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="be164-138">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="be164-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be164-139">-ResourceGroupName</span></span>
<span data-ttu-id="be164-140">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="be164-140">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="be164-141">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="be164-141">-SecretIdentifier</span></span>
<span data-ttu-id="be164-142">Var olan Azure Key kasa parolası URI 'si.</span><span class="sxs-lookup"><span data-stu-id="be164-142">The existing Azure key vault secret uri.</span></span>

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

### <span data-ttu-id="be164-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="be164-143">-Confirm</span></span>
<span data-ttu-id="be164-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="be164-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be164-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be164-145">-WhatIf</span></span>
<span data-ttu-id="be164-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="be164-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be164-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="be164-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be164-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be164-148">CommonParameters</span></span>
<span data-ttu-id="be164-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be164-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be164-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be164-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be164-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be164-151">INPUTS</span></span>

### <span data-ttu-id="be164-152">System. String</span><span class="sxs-lookup"><span data-stu-id="be164-152">System.String</span></span>

### <span data-ttu-id="be164-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="be164-153">System.Security.SecureString</span></span>

## <span data-ttu-id="be164-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be164-154">OUTPUTS</span></span>

### <span data-ttu-id="be164-155">Microsoft. Azure. Commands. ServiceFabric. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="be164-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="be164-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be164-156">NOTES</span></span>

## <span data-ttu-id="be164-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be164-157">RELATED LINKS</span></span>

[<span data-ttu-id="be164-158">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="be164-158">Add-AzServiceFabricClusterCertificate</span></span>](./Add-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="be164-159">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="be164-159">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
