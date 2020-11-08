---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 36ed679066d1850851ff0e90f39eb6f9ef8ffa1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275682"
---
# <span data-ttu-id="d8867-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="d8867-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="d8867-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8867-102">SYNOPSIS</span></span>
<span data-ttu-id="d8867-103">Düğüm türüne sertifika parolası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d8867-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="d8867-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8867-104">SYNTAX</span></span>

### <span data-ttu-id="d8867-105">ByObj (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d8867-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8867-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d8867-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8867-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8867-107">DESCRIPTION</span></span>
<span data-ttu-id="d8867-108">Düğüm türüne sertifika parolası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d8867-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="d8867-109">Gizlilik, bir Azure Anahtar Kasası 'nda depolanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d8867-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="d8867-110">Anahtar Kasası ile ilgili daha fazla bilgi için Azure Anahtar Kasası nedir?</span><span class="sxs-lookup"><span data-stu-id="d8867-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="d8867-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="d8867-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="d8867-112">Cmdlet 'ler hakkında daha fazla bilgi için Azure Anahtar Kasası cmdlet 'Lerini ( https://msdn.microsoft.com/library/azure/dn868052.aspx) Microsoft Developer Network Library veya Set-AzKeyVaultSecret cmdlet 'inde görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8867-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="d8867-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8867-113">EXAMPLES</span></span>

### <span data-ttu-id="d8867-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d8867-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="d8867-115">Bu CommAd, anahtar kasası ve belirtilen gizli tanımlayıcıdan sertifika parolası ekler.</span><span class="sxs-lookup"><span data-stu-id="d8867-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="d8867-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d8867-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="d8867-117">Bu CommAd, borular ile belirtilen keykasası ve gizli tanımlayıcısından sertifika parolası ekler.</span><span class="sxs-lookup"><span data-stu-id="d8867-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="d8867-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8867-118">PARAMETERS</span></span>

### <span data-ttu-id="d8867-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="d8867-119">-AsJob</span></span>
<span data-ttu-id="d8867-120">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="d8867-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d8867-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="d8867-121">-CertificateStore</span></span>
<span data-ttu-id="d8867-122">Sertifikanın ekleneceği sanal makinedeki sertifika deposunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8867-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="d8867-123">Belirtilen sertifika deposu, LocalMachine hesabında örtük olarak.</span><span class="sxs-lookup"><span data-stu-id="d8867-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

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

### <span data-ttu-id="d8867-124">-CertificateUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="d8867-124">-CertificateUrl</span></span>
<span data-ttu-id="d8867-125">Bu, anahtar kasasına parola olarak yüklenen sertifikanın URL 'sidir.</span><span class="sxs-lookup"><span data-stu-id="d8867-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="d8867-126">Anahtar kasasına gizli kod eklemek için, \[ anahtar kasasına anahtar veya gizli ekleme bölümüne bakın \] https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) .</span><span class="sxs-lookup"><span data-stu-id="d8867-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="d8867-127">Bu durumda, sertifikanızın, UTF-8 ' i kodlanmış aşağıdaki JSON nesnesinin Base64 kodlaması olması gereklidir: \<br\> \<br\> { \<br\> "Data": " \<Base64-encoded-certificate\> ", \<br\> "DataType": "PFX", \<br\> "Password": " \<pfx-file-password\> " \<br\> }/</span><span class="sxs-lookup"><span data-stu-id="d8867-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

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

### <span data-ttu-id="d8867-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d8867-128">-ClusterName</span></span>
<span data-ttu-id="d8867-129">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d8867-129">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8867-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8867-130">-DefaultProfile</span></span>
<span data-ttu-id="d8867-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8867-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8867-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8867-132">-InputObject</span></span>
<span data-ttu-id="d8867-133">Düğüm türü kaynağı</span><span class="sxs-lookup"><span data-stu-id="d8867-133">Node Type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8867-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8867-134">-Name</span></span>
<span data-ttu-id="d8867-135">Düğüm türünün adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d8867-135">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8867-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8867-136">-ResourceGroupName</span></span>
<span data-ttu-id="d8867-137">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d8867-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8867-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="d8867-138">-SourceVaultId</span></span>
<span data-ttu-id="d8867-139">Sertifikaları içeren Anahtar Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d8867-139">Key Vault resource id containing the certificates.</span></span>

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

### <span data-ttu-id="d8867-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="d8867-140">-Confirm</span></span>
<span data-ttu-id="d8867-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d8867-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8867-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8867-142">-WhatIf</span></span>
<span data-ttu-id="d8867-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8867-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8867-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d8867-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8867-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8867-145">CommonParameters</span></span>
<span data-ttu-id="d8867-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8867-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8867-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d8867-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8867-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8867-148">INPUTS</span></span>

### <span data-ttu-id="d8867-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d8867-149">System.String</span></span>

## <span data-ttu-id="d8867-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8867-150">OUTPUTS</span></span>

### <span data-ttu-id="d8867-151">Microsoft. Azure. Commands. ServiceFabric. modeller. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="d8867-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="d8867-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8867-152">NOTES</span></span>

## <span data-ttu-id="d8867-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8867-153">RELATED LINKS</span></span>
