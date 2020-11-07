---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
ms.openlocfilehash: 62298a5747a8bb5b4f01458cac611f5e86869ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933206"
---
# <span data-ttu-id="c2871-101">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="c2871-101">Add-AzServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="c2871-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2871-102">SYNOPSIS</span></span>
<span data-ttu-id="c2871-103">Kümeyi oluşturan sanal makine ölçek kümesine yeni bir sertifika ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c2871-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="c2871-104">Sertifika, uygulama sertifikası olarak kullanılmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c2871-104">The certificate is intended to be used as an application certificate.</span></span>

## <span data-ttu-id="c2871-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2871-105">SYNTAX</span></span>

### <span data-ttu-id="c2871-106">Varexistingtuş Kasası</span><span class="sxs-lookup"><span data-stu-id="c2871-106">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2871-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="c2871-107">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2871-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="c2871-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2871-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2871-109">DESCRIPTION</span></span>
<span data-ttu-id="c2871-110">Kümedeki tüm düğümlere sertifika yüklemek için **Add-AzServiceFabricApplicationCertificate** kullanın.</span><span class="sxs-lookup"><span data-stu-id="c2871-110">Use **Add-AzServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="c2871-111">Zaten sahip olduğunuz bir sertifikayı belirtebilir ya da sistemin sizin için yeni bir sertifika üretmesine ve yeni veya mevcut bir Azure anahtar kasasına yüklemesini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c2871-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="c2871-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2871-112">EXAMPLES</span></span>

### <span data-ttu-id="c2871-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c2871-113">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="c2871-114">Bu komut, var olan Azure Key kasasından kümenin tüm düğüm türlerine sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="c2871-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="c2871-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c2871-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="c2871-116">Bu komut, Azure Anahtar Kasası 'nda Anahtar Kasası kaynak grubu adı ve Anahtar Kasası adı olan kendinden imzalanan bir sertifika oluşturur, kümenin tüm düğüm türlerine yükler ve ' c:\Test ' klasörünün altında sertifikayı indirir.</span><span class="sxs-lookup"><span data-stu-id="c2871-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="c2871-117">İndirilen sertifikanın adı, Anahtar Kasası sertifikasının adıyla aynıdır.</span><span class="sxs-lookup"><span data-stu-id="c2871-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="c2871-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2871-118">PARAMETERS</span></span>

### <span data-ttu-id="c2871-119">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="c2871-119">-CertificateCommonName</span></span>
<span data-ttu-id="c2871-120">Sertifika ortak adı</span><span class="sxs-lookup"><span data-stu-id="c2871-120">Certificate common name</span></span>

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

### <span data-ttu-id="c2871-121">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c2871-121">-CertificateFile</span></span>
<span data-ttu-id="c2871-122">Var olan sertifikanın yolu</span><span class="sxs-lookup"><span data-stu-id="c2871-122">The path to the existing certificate</span></span>

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

### <span data-ttu-id="c2871-123">-Certificateıssuerparmak Izi</span><span class="sxs-lookup"><span data-stu-id="c2871-123">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="c2871-124">Birden çok sayıda virgül ile ayrılmış sertifika veren parmak izi</span><span class="sxs-lookup"><span data-stu-id="c2871-124">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="c2871-125">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="c2871-125">-CertificateOutputFolder</span></span>
<span data-ttu-id="c2871-126">Yeni sertifikanın yüklenmesi gerektiği klasör.</span><span class="sxs-lookup"><span data-stu-id="c2871-126">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="c2871-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c2871-127">-CertificatePassword</span></span>
<span data-ttu-id="c2871-128">Sertifikanın parolası</span><span class="sxs-lookup"><span data-stu-id="c2871-128">The password of the certificate</span></span>

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

### <span data-ttu-id="c2871-129">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="c2871-129">-CertificateSubjectName</span></span>
<span data-ttu-id="c2871-130">Sertifikanın konu adı</span><span class="sxs-lookup"><span data-stu-id="c2871-130">The subject name of the certificate</span></span>

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

### <span data-ttu-id="c2871-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2871-131">-DefaultProfile</span></span>
<span data-ttu-id="c2871-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2871-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2871-133">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="c2871-133">-KeyVaultName</span></span>
<span data-ttu-id="c2871-134">Azure Anahtar Kasası adı verilmezse, kaynak grubu adına varsayılan olarak alınır</span><span class="sxs-lookup"><span data-stu-id="c2871-134">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="c2871-135">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2871-135">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="c2871-136">Verilmezse Azure Anahtar Kasası kaynak grubu adı, kaynak grubu adına varsayılan olarak alınır</span><span class="sxs-lookup"><span data-stu-id="c2871-136">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2871-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="c2871-137">-Name</span></span>
<span data-ttu-id="c2871-138">Kümenin adını belirtme</span><span class="sxs-lookup"><span data-stu-id="c2871-138">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="c2871-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2871-139">-ResourceGroupName</span></span>
<span data-ttu-id="c2871-140">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="c2871-140">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c2871-141">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="c2871-141">-SecretIdentifier</span></span>
<span data-ttu-id="c2871-142">Var olan Azure Key kasa gizli URL 'SI; örneğin ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="c2871-142">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="c2871-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="c2871-143">-Confirm</span></span>
<span data-ttu-id="c2871-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c2871-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2871-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2871-145">-WhatIf</span></span>
<span data-ttu-id="c2871-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2871-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2871-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c2871-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2871-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2871-148">CommonParameters</span></span>
<span data-ttu-id="c2871-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2871-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2871-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2871-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2871-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2871-151">INPUTS</span></span>

### <span data-ttu-id="c2871-152">System. String</span><span class="sxs-lookup"><span data-stu-id="c2871-152">System.String</span></span>

### <span data-ttu-id="c2871-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="c2871-153">System.Security.SecureString</span></span>

## <span data-ttu-id="c2871-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2871-154">OUTPUTS</span></span>

### <span data-ttu-id="c2871-155">Microsoft. Azure. Commands. ServiceFabric. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="c2871-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="c2871-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2871-156">NOTES</span></span>

## <span data-ttu-id="c2871-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2871-157">RELATED LINKS</span></span>

[<span data-ttu-id="c2871-158">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="c2871-158">Add-AzServiceFabricClusterCertificate</span></span>](./Add-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="c2871-159">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c2871-159">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
