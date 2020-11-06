---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
ms.openlocfilehash: 6d77c795415bca1a8bffbed6d09062f394782e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593794"
---
# <span data-ttu-id="2b1e2-101">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="2b1e2-101">Add-AzureRmServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="2b1e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b1e2-102">SYNOPSIS</span></span>
<span data-ttu-id="2b1e2-103">Kümeyi oluşturan sanal makine ölçek kümesine yeni bir sertifika ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="2b1e2-104">Sertifika, uygulama sertifikası olarak kullanılmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-104">The certificate is intended to be used as an application certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b1e2-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b1e2-105">SYNTAX</span></span>

### <span data-ttu-id="2b1e2-106">Varexistingtuş Kasası</span><span class="sxs-lookup"><span data-stu-id="2b1e2-106">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b1e2-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="2b1e2-107">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b1e2-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="2b1e2-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b1e2-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b1e2-109">DESCRIPTION</span></span>
<span data-ttu-id="2b1e2-110">Kümedeki tüm düğümlere sertifika yüklemek için **Add-AzureRmServiceFabricApplicationCertificate** öğesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-110">Use **Add-AzureRmServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="2b1e2-111">Zaten sahip olduğunuz bir sertifikayı belirtebilir ya da sistemin sizin için yeni bir sertifika üretmesine ve yeni veya mevcut bir Azure anahtar kasasına yüklemesini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="2b1e2-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b1e2-112">EXAMPLES</span></span>

### <span data-ttu-id="2b1e2-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2b1e2-113">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="2b1e2-114">Bu komut, var olan Azure Key kasasından kümenin tüm düğüm türlerine sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="2b1e2-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2b1e2-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="2b1e2-116">Bu komut, Azure Anahtar Kasası 'nda Anahtar Kasası kaynak grubu adı ve Anahtar Kasası adı olan kendinden imzalanan bir sertifika oluşturur, kümenin tüm düğüm türlerine yükler ve ' c:\Test ' klasörünün altında sertifikayı indirir.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="2b1e2-117">İndirilen sertifikanın adı, Anahtar Kasası sertifikasının adıyla aynıdır.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="2b1e2-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b1e2-118">PARAMETERS</span></span>

### <span data-ttu-id="2b1e2-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="2b1e2-119">-CertificateFile</span></span>
<span data-ttu-id="2b1e2-120">Var olan sertifika dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="2b1e2-121">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="2b1e2-121">-CertificateOutputFolder</span></span>
<span data-ttu-id="2b1e2-122">Oluşturulacak yeni sertifikanın klasör yolu.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-122">The folder path of the new certificate to be created.</span></span>

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

### <span data-ttu-id="2b1e2-123">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="2b1e2-123">-CertificatePassword</span></span>
<span data-ttu-id="2b1e2-124">Pfx dosyasının parolası.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-124">The password of the pfx file.</span></span>

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

### <span data-ttu-id="2b1e2-125">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="2b1e2-125">-CertificateSubjectName</span></span>
<span data-ttu-id="2b1e2-126">Oluşturulacak sertifikanın DNS adı.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-126">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="2b1e2-127">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="2b1e2-127">-KeyVaultName</span></span>
<span data-ttu-id="2b1e2-128">Azure Key kasa adı.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-128">Azure key vault name.</span></span>

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

### <span data-ttu-id="2b1e2-129">-Keyvaultbalanucegroupname</span><span class="sxs-lookup"><span data-stu-id="2b1e2-129">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="2b1e2-130">Azure Key kasa kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-130">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="2b1e2-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="2b1e2-131">-Name</span></span>
<span data-ttu-id="2b1e2-132">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-132">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2b1e2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b1e2-133">-ResourceGroupName</span></span>
<span data-ttu-id="2b1e2-134">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2b1e2-135">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="2b1e2-135">-SecretIdentifier</span></span>
<span data-ttu-id="2b1e2-136">Var olan Azure Key kasa parolası URI 'si.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-136">The existing Azure key vault secret uri.</span></span>

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

### <span data-ttu-id="2b1e2-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="2b1e2-137">-Confirm</span></span>
<span data-ttu-id="2b1e2-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b1e2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b1e2-139">-WhatIf</span></span>
<span data-ttu-id="2b1e2-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b1e2-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b1e2-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b1e2-142">-DefaultProfile</span></span>
<span data-ttu-id="2b1e2-143">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b1e2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b1e2-144">CommonParameters</span></span>
<span data-ttu-id="2b1e2-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b1e2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b1e2-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b1e2-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b1e2-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b1e2-147">INPUTS</span></span>

### <span data-ttu-id="2b1e2-148">System. String</span><span class="sxs-lookup"><span data-stu-id="2b1e2-148">System.String</span></span>

## <span data-ttu-id="2b1e2-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b1e2-149">OUTPUTS</span></span>

### <span data-ttu-id="2b1e2-150">Microsoft. Azure. Commands. ServiceFabric. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="2b1e2-150">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="2b1e2-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b1e2-151">NOTES</span></span>

## <span data-ttu-id="2b1e2-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b1e2-152">RELATED LINKS</span></span>

[<span data-ttu-id="2b1e2-153">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2b1e2-153">Add-AzureRmServiceFabricClusterCertificate</span></span>](./Add-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="2b1e2-154">Yeni-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="2b1e2-154">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)
