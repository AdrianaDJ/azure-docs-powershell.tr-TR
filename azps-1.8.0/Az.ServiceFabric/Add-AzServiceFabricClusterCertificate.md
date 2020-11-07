---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: bf96b4a21e12e41ce067d669b50c05831a162a8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759125"
---
# <span data-ttu-id="e04a0-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="e04a0-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="e04a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e04a0-102">SYNOPSIS</span></span>
<span data-ttu-id="e04a0-103">Kümeye ikincil küme sertifikası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e04a0-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="e04a0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e04a0-104">SYNTAX</span></span>

### <span data-ttu-id="e04a0-105">Varexistingtuş Kasası</span><span class="sxs-lookup"><span data-stu-id="e04a0-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e04a0-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="e04a0-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e04a0-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="e04a0-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e04a0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e04a0-108">DESCRIPTION</span></span>
<span data-ttu-id="e04a0-109">**Add-AzServiceFabricClusterCertificate** öğesini kullanarak, var olan bir Azure Anahtar Kasası 'ndan veya varolan bir sertifikayı veya yeni bir otomatik olarak imzalanan sertifikadan oluşturulan bir Azure Anahtar Kasası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e04a0-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="e04a0-110">Varsa ikincil kümeyi geçersiz kılacaktır.</span><span class="sxs-lookup"><span data-stu-id="e04a0-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="e04a0-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e04a0-111">EXAMPLES</span></span>

### <span data-ttu-id="e04a0-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e04a0-112">Example 1</span></span>
```
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="e04a0-113">Bu komut, var olan Azure Key kasasına ikincil küme sertifikası olarak bir sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="e04a0-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="e04a0-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e04a0-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="e04a0-115">Bu komut, Azure Anahtar Kasası 'nda otomatik olarak imzalanan bir sertifika oluşturur ve kümeyi ikincil bir küme sertifikası olarak kullanmak üzere yükseltir.</span><span class="sxs-lookup"><span data-stu-id="e04a0-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="e04a0-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e04a0-116">PARAMETERS</span></span>

### <span data-ttu-id="e04a0-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="e04a0-117">-CertificateCommonName</span></span>
<span data-ttu-id="e04a0-118">Sertifika ortak adı</span><span class="sxs-lookup"><span data-stu-id="e04a0-118">Certificate common name</span></span>

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

### <span data-ttu-id="e04a0-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e04a0-119">-CertificateFile</span></span>
<span data-ttu-id="e04a0-120">Var olan sertifika dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="e04a0-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="e04a0-121">-Certificateıssuerparmak Izi</span><span class="sxs-lookup"><span data-stu-id="e04a0-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="e04a0-122">Birden çok sayıda virgül ile ayrılmış sertifika veren parmak izi</span><span class="sxs-lookup"><span data-stu-id="e04a0-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="e04a0-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="e04a0-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="e04a0-124">Oluşturulacak yeni sertifikanın klasörü.</span><span class="sxs-lookup"><span data-stu-id="e04a0-124">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="e04a0-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e04a0-125">-CertificatePassword</span></span>
<span data-ttu-id="e04a0-126">Sertifika dosyasının parolası.</span><span class="sxs-lookup"><span data-stu-id="e04a0-126">The password of the certificate file.</span></span>

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

### <span data-ttu-id="e04a0-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="e04a0-127">-CertificateSubjectName</span></span>
<span data-ttu-id="e04a0-128">Oluşturulacak sertifikanın DNS adı.</span><span class="sxs-lookup"><span data-stu-id="e04a0-128">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="e04a0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e04a0-129">-DefaultProfile</span></span>
<span data-ttu-id="e04a0-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e04a0-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e04a0-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="e04a0-131">-KeyVaultName</span></span>
<span data-ttu-id="e04a0-132">Azure Key kasa adı.</span><span class="sxs-lookup"><span data-stu-id="e04a0-132">Azure key vault name.</span></span>

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

### <span data-ttu-id="e04a0-133">-Keyvaultbalanucegroupname</span><span class="sxs-lookup"><span data-stu-id="e04a0-133">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="e04a0-134">Azure Key kasa kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e04a0-134">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="e04a0-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="e04a0-135">-Name</span></span>
<span data-ttu-id="e04a0-136">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="e04a0-136">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e04a0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e04a0-137">-ResourceGroupName</span></span>
<span data-ttu-id="e04a0-138">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e04a0-138">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e04a0-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="e04a0-139">-SecretIdentifier</span></span>
<span data-ttu-id="e04a0-140">Var olan Azure Key kasa gizli URL 'Si.</span><span class="sxs-lookup"><span data-stu-id="e04a0-140">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="e04a0-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="e04a0-141">-Confirm</span></span>
<span data-ttu-id="e04a0-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e04a0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e04a0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e04a0-143">-WhatIf</span></span>
<span data-ttu-id="e04a0-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e04a0-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e04a0-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e04a0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e04a0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e04a0-146">CommonParameters</span></span>
<span data-ttu-id="e04a0-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e04a0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e04a0-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e04a0-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e04a0-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e04a0-149">INPUTS</span></span>

### <span data-ttu-id="e04a0-150">System. String</span><span class="sxs-lookup"><span data-stu-id="e04a0-150">System.String</span></span>

### <span data-ttu-id="e04a0-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e04a0-151">System.Security.SecureString</span></span>

## <span data-ttu-id="e04a0-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e04a0-152">OUTPUTS</span></span>

### <span data-ttu-id="e04a0-153">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="e04a0-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="e04a0-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e04a0-154">NOTES</span></span>

## <span data-ttu-id="e04a0-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e04a0-155">RELATED LINKS</span></span>

[<span data-ttu-id="e04a0-156">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="e04a0-156">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="e04a0-157">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="e04a0-157">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)

[<span data-ttu-id="e04a0-158">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="e04a0-158">Add-AzServiceFabricApplicationCertificate</span></span>](./Add-AzServiceFabricApplicationCertificate.md)
