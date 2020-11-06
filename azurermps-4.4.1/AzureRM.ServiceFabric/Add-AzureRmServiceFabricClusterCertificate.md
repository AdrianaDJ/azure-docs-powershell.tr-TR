---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: 498b09867436e6aa272abd8796b41f159cd388f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593793"
---
# <span data-ttu-id="f747d-101">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f747d-101">Add-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="f747d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f747d-102">SYNOPSIS</span></span>
<span data-ttu-id="f747d-103">Kümeye ikincil küme sertifikası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f747d-103">Add a secondary cluster certificate to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f747d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f747d-104">SYNTAX</span></span>

### <span data-ttu-id="f747d-105">Varexistingtuş Kasası</span><span class="sxs-lookup"><span data-stu-id="f747d-105">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f747d-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="f747d-106">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f747d-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="f747d-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f747d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f747d-108">DESCRIPTION</span></span>
<span data-ttu-id="f747d-109">**Add-AzureRmServiceFabricClusterCertificate** öğesini kullanarak, var olan bir Azure Anahtar Kasası 'ndan veya varolan bir sertifikayı kullanarak varolan bir Azure Anahtar Kasası oluşturabilir</span><span class="sxs-lookup"><span data-stu-id="f747d-109">Use **Add-AzureRmServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="f747d-110">Varsa ikincil kümeyi geçersiz kılacaktır.</span><span class="sxs-lookup"><span data-stu-id="f747d-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="f747d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f747d-111">EXAMPLES</span></span>

### <span data-ttu-id="f747d-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f747d-112">Example 1</span></span>
```
Add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="f747d-113">Bu komut, var olan Azure Key kasasına ikincil küme sertifikası olarak bir sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="f747d-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="f747d-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f747d-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="f747d-115">Bu komut, Azure Anahtar Kasası 'nda otomatik olarak imzalanan bir sertifika oluşturur ve kümeyi ikincil bir küme sertifikası olarak kullanmak üzere yükseltir.</span><span class="sxs-lookup"><span data-stu-id="f747d-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="f747d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f747d-116">PARAMETERS</span></span>

### <span data-ttu-id="f747d-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f747d-117">-CertificateFile</span></span>
<span data-ttu-id="f747d-118">Var olan sertifika dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="f747d-118">The existing certificate file path.</span></span>

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

### <span data-ttu-id="f747d-119">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="f747d-119">-CertificateOutputFolder</span></span>
<span data-ttu-id="f747d-120">Oluşturulacak yeni sertifikanın klasörü.</span><span class="sxs-lookup"><span data-stu-id="f747d-120">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="f747d-121">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f747d-121">-CertificatePassword</span></span>
<span data-ttu-id="f747d-122">Sertifika dosyasının parolası.</span><span class="sxs-lookup"><span data-stu-id="f747d-122">The password of the certificate file.</span></span>

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

### <span data-ttu-id="f747d-123">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="f747d-123">-CertificateSubjectName</span></span>
<span data-ttu-id="f747d-124">Oluşturulacak sertifikanın DNS adı.</span><span class="sxs-lookup"><span data-stu-id="f747d-124">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="f747d-125">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="f747d-125">-KeyVaultName</span></span>
<span data-ttu-id="f747d-126">Azure Key kasa adı.</span><span class="sxs-lookup"><span data-stu-id="f747d-126">Azure key vault name.</span></span>

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

### <span data-ttu-id="f747d-127">-Keyvaultbalanucegroupname</span><span class="sxs-lookup"><span data-stu-id="f747d-127">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="f747d-128">Azure Key kasa kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f747d-128">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="f747d-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="f747d-129">-Name</span></span>
<span data-ttu-id="f747d-130">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="f747d-130">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="f747d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f747d-131">-ResourceGroupName</span></span>
<span data-ttu-id="f747d-132">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f747d-132">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f747d-133">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="f747d-133">-SecretIdentifier</span></span>
<span data-ttu-id="f747d-134">Var olan Azure Key kasa gizli URL 'Si.</span><span class="sxs-lookup"><span data-stu-id="f747d-134">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="f747d-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="f747d-135">-Confirm</span></span>
<span data-ttu-id="f747d-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f747d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f747d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f747d-137">-WhatIf</span></span>
<span data-ttu-id="f747d-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f747d-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f747d-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f747d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f747d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f747d-140">-DefaultProfile</span></span>
<span data-ttu-id="f747d-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f747d-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f747d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f747d-142">CommonParameters</span></span>
<span data-ttu-id="f747d-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f747d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f747d-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f747d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f747d-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f747d-145">INPUTS</span></span>

### <span data-ttu-id="f747d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f747d-146">System.String</span></span>

## <span data-ttu-id="f747d-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f747d-147">OUTPUTS</span></span>

### <span data-ttu-id="f747d-148">Microsoft. Azure. Commands. ServiceFabric. modeller. PsCluster</span><span class="sxs-lookup"><span data-stu-id="f747d-148">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="f747d-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f747d-149">NOTES</span></span>

## <span data-ttu-id="f747d-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f747d-150">RELATED LINKS</span></span>

[<span data-ttu-id="f747d-151">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f747d-151">Remove-AzureRmServiceFabricClusterCertificate</span></span>](./Remove-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="f747d-152">Yeni-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="f747d-152">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)

[<span data-ttu-id="f747d-153">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="f747d-153">Add-AzureRmServiceFabricApplicationCertificate</span></span>](./Add-AzureRmServiceFabricApplicationCertificate.md)
