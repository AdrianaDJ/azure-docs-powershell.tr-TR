---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: c7b6e00ccbe368267fd6b110490df4f70b2229a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592397"
---
# <span data-ttu-id="90e00-101">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="90e00-101">Add-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="90e00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90e00-102">SYNOPSIS</span></span>
<span data-ttu-id="90e00-103">İstemci kimlik doğrulama amaçları için kümeye ortak ad veya parmak izi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="90e00-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90e00-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90e00-104">SYNTAX</span></span>

### <span data-ttu-id="90e00-105">Singleupdatewithparmak Izi</span><span class="sxs-lookup"><span data-stu-id="90e00-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90e00-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="90e00-106">SingleUpdateWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90e00-107">Multipleupdateswithname</span><span class="sxs-lookup"><span data-stu-id="90e00-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90e00-108">Çoğulgüncelleştirmeleriwithparmak Izi</span><span class="sxs-lookup"><span data-stu-id="90e00-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90e00-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="90e00-109">DESCRIPTION</span></span>
<span data-ttu-id="90e00-110">Bir ortak ad ve veren parmak izi veya sertifika parmak izi eklemek için **Add-AzureRmServiceFabricClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="90e00-110">Use **Add-AzureRmServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="90e00-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90e00-111">EXAMPLES</span></span>

### <span data-ttu-id="90e00-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="90e00-112">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="90e00-113">Bu komut, ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' parmak izine sahip sertifikayı kümeye ekler; böylece istemci kümeyle iletişim kurmak için sertifikayı yönetici olarak kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="90e00-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="90e00-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="90e00-114">Example 2</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="90e00-115">Bu komut, ortak adı salt okunur bir istemci sertifikası ekler ' Contoso.com ' ve Issuer parmak izi ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A '.</span><span class="sxs-lookup"><span data-stu-id="90e00-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="90e00-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90e00-116">PARAMETERS</span></span>

### <span data-ttu-id="90e00-117">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="90e00-117">-Admin</span></span>
<span data-ttu-id="90e00-118">İstemci kimlik doğrulama türü.</span><span class="sxs-lookup"><span data-stu-id="90e00-118">Client authentication type.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e00-119">-Adminclientparmak Izi</span><span class="sxs-lookup"><span data-stu-id="90e00-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="90e00-120">Yalnızca yönetici izni olan istemci sertifikası parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="90e00-120">Specify client certificate thumbprint that only has admin permission.</span></span>

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e00-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="90e00-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="90e00-122">İstemci ortak adını, verenin parmak izini ve kimlik doğrulama türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="90e00-122">Specify client common name, issuer thumbprint, and authentication type.</span></span>

```yaml
Type: PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e00-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="90e00-123">-CommonName</span></span>
<span data-ttu-id="90e00-124">İstemci sertifikası ortak adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="90e00-124">Specify client certificate common name.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e00-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e00-125">-DefaultProfile</span></span>
<span data-ttu-id="90e00-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="90e00-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e00-127">-Issuerparmak Izi</span><span class="sxs-lookup"><span data-stu-id="90e00-127">-IssuerThumbprint</span></span>
<span data-ttu-id="90e00-128">İstemci sertifikası verenin parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="90e00-128">Specify client certificate issuer thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e00-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="90e00-129">-Name</span></span>
<span data-ttu-id="90e00-130">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="90e00-130">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e00-131">-Readonlyclientparmak Izi</span><span class="sxs-lookup"><span data-stu-id="90e00-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="90e00-132">Salt okunur izni olan istemci sertifikası parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="90e00-132">Specify client certificate thumbprint that has read only permission.</span></span>

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e00-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e00-133">-ResourceGroupName</span></span>
<span data-ttu-id="90e00-134">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90e00-134">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e00-135">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="90e00-135">-Thumbprint</span></span>
<span data-ttu-id="90e00-136">İstemci sertifikası parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="90e00-136">Specify client certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e00-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="90e00-137">-Confirm</span></span>
<span data-ttu-id="90e00-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="90e00-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e00-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e00-139">-WhatIf</span></span>
<span data-ttu-id="90e00-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="90e00-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90e00-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="90e00-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e00-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e00-142">CommonParameters</span></span>
<span data-ttu-id="90e00-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90e00-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e00-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90e00-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e00-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90e00-145">INPUTS</span></span>

### <span data-ttu-id="90e00-146">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="90e00-146">System.Collections.Hashtable</span></span>
<span data-ttu-id="90e00-147">System. String</span><span class="sxs-lookup"><span data-stu-id="90e00-147">System.String</span></span>

<span data-ttu-id="90e00-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90e00-148">System.Boolean</span></span>

## <span data-ttu-id="90e00-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90e00-149">OUTPUTS</span></span>

### <span data-ttu-id="90e00-150">Microsoft. Azure. Commands. ServiceFabric. modeller. PsCluster</span><span class="sxs-lookup"><span data-stu-id="90e00-150">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="90e00-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90e00-151">NOTES</span></span>

## <span data-ttu-id="90e00-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90e00-152">RELATED LINKS</span></span>

[<span data-ttu-id="90e00-153">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="90e00-153">Remove-AzureRmServiceFabricClientCertificate</span></span>](./Remove-AzureRmServiceFabricClientCertificate.md)
