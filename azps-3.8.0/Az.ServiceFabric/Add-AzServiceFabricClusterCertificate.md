---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: dfbf9267aad981db63608c744825f1b636c85425
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096553"
---
# <span data-ttu-id="cff86-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="cff86-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="cff86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cff86-102">SYNOPSIS</span></span>
<span data-ttu-id="cff86-103">Kümeye ikincil küme sertifikası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="cff86-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="cff86-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cff86-104">SYNTAX</span></span>

### <span data-ttu-id="cff86-105">Varexistingtuş Kasası</span><span class="sxs-lookup"><span data-stu-id="cff86-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cff86-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="cff86-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cff86-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="cff86-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cff86-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cff86-108">DESCRIPTION</span></span>
<span data-ttu-id="cff86-109">**Add-AzServiceFabricClusterCertificate** öğesini kullanarak, var olan bir Azure Anahtar Kasası 'ndan veya varolan bir sertifikayı veya yeni bir otomatik olarak imzalanan sertifikadan oluşturulan bir Azure Anahtar Kasası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="cff86-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="cff86-110">Varsa ikincil kümeyi geçersiz kılacaktır.</span><span class="sxs-lookup"><span data-stu-id="cff86-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="cff86-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cff86-111">EXAMPLES</span></span>

### <span data-ttu-id="cff86-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cff86-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="cff86-113">Bu komut, var olan Azure Key kasasına ikincil küme sertifikası olarak bir sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="cff86-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="cff86-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cff86-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="cff86-115">Bu komut, Azure Anahtar Kasası 'nda otomatik olarak imzalanan bir sertifika oluşturur ve kümeyi ikincil bir küme sertifikası olarak kullanmak üzere yükseltir.</span><span class="sxs-lookup"><span data-stu-id="cff86-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="cff86-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cff86-116">PARAMETERS</span></span>

### <span data-ttu-id="cff86-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="cff86-117">-CertificateCommonName</span></span>
<span data-ttu-id="cff86-118">Sertifika ortak adı</span><span class="sxs-lookup"><span data-stu-id="cff86-118">Certificate common name</span></span>

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

### <span data-ttu-id="cff86-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="cff86-119">-CertificateFile</span></span>
<span data-ttu-id="cff86-120">Var olan sertifikanın yolu</span><span class="sxs-lookup"><span data-stu-id="cff86-120">The path to the existing certificate</span></span>

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

### <span data-ttu-id="cff86-121">-Certificateıssuerparmak Izi</span><span class="sxs-lookup"><span data-stu-id="cff86-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="cff86-122">Birden çok sayıda virgül ile ayrılmış sertifika veren parmak izi</span><span class="sxs-lookup"><span data-stu-id="cff86-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="cff86-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="cff86-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="cff86-124">Yeni sertifikanın yüklenmesi gerektiği klasör.</span><span class="sxs-lookup"><span data-stu-id="cff86-124">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="cff86-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="cff86-125">-CertificatePassword</span></span>
<span data-ttu-id="cff86-126">Sertifikanın parolası</span><span class="sxs-lookup"><span data-stu-id="cff86-126">The password of the certificate</span></span>

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

### <span data-ttu-id="cff86-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="cff86-127">-CertificateSubjectName</span></span>
<span data-ttu-id="cff86-128">Sertifikanın konu adı</span><span class="sxs-lookup"><span data-stu-id="cff86-128">The subject name of the certificate</span></span>

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

### <span data-ttu-id="cff86-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff86-129">-DefaultProfile</span></span>
<span data-ttu-id="cff86-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cff86-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cff86-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="cff86-131">-KeyVaultName</span></span>
<span data-ttu-id="cff86-132">Azure Anahtar Kasası adı verilmezse, kaynak grubu adına varsayılan olarak alınır</span><span class="sxs-lookup"><span data-stu-id="cff86-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="cff86-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cff86-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="cff86-134">Verilmezse Azure Anahtar Kasası kaynak grubu adı, kaynak grubu adına varsayılan olarak alınır</span><span class="sxs-lookup"><span data-stu-id="cff86-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="cff86-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="cff86-135">-Name</span></span>
<span data-ttu-id="cff86-136">Kümenin adını belirtme</span><span class="sxs-lookup"><span data-stu-id="cff86-136">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="cff86-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cff86-137">-ResourceGroupName</span></span>
<span data-ttu-id="cff86-138">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="cff86-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="cff86-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="cff86-139">-SecretIdentifier</span></span>
<span data-ttu-id="cff86-140">Var olan Azure Key kasa gizli URL 'SI; örneğin ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="cff86-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="cff86-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="cff86-141">-Confirm</span></span>
<span data-ttu-id="cff86-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cff86-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cff86-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cff86-143">-WhatIf</span></span>
<span data-ttu-id="cff86-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cff86-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cff86-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cff86-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cff86-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff86-146">CommonParameters</span></span>
<span data-ttu-id="cff86-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cff86-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff86-148">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cff86-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff86-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cff86-149">INPUTS</span></span>

### <span data-ttu-id="cff86-150">System. String</span><span class="sxs-lookup"><span data-stu-id="cff86-150">System.String</span></span>

### <span data-ttu-id="cff86-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="cff86-151">System.Security.SecureString</span></span>

## <span data-ttu-id="cff86-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cff86-152">OUTPUTS</span></span>

### <span data-ttu-id="cff86-153">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="cff86-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="cff86-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cff86-154">NOTES</span></span>

## <span data-ttu-id="cff86-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cff86-155">RELATED LINKS</span></span>

[<span data-ttu-id="cff86-156">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="cff86-156">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="cff86-157">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="cff86-157">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
