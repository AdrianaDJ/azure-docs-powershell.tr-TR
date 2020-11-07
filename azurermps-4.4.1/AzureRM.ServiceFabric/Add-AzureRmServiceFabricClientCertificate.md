---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: 37db0181ea135a0cdb00cddc0a18780fe9fe2d7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764222"
---
# <span data-ttu-id="b695d-101">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b695d-101">Add-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="b695d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b695d-102">SYNOPSIS</span></span>
<span data-ttu-id="b695d-103">İstemci kimlik doğrulama amaçları için kümeye ortak ad veya parmak izi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b695d-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b695d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b695d-104">SYNTAX</span></span>

### <span data-ttu-id="b695d-105">Singleupdatewithparmak Izi</span><span class="sxs-lookup"><span data-stu-id="b695d-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b695d-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="b695d-106">SingleUpdateWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b695d-107">Multipleupdateswithname</span><span class="sxs-lookup"><span data-stu-id="b695d-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b695d-108">Çoğulgüncelleştirmeleriwithparmak Izi</span><span class="sxs-lookup"><span data-stu-id="b695d-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b695d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b695d-109">DESCRIPTION</span></span>
<span data-ttu-id="b695d-110">Bir ortak ad ve veren parmak izi veya sertifika parmak izi eklemek için **Add-AzureRmServiceFabricClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="b695d-110">Use **Add-AzureRmServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="b695d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b695d-111">EXAMPLES</span></span>

### <span data-ttu-id="b695d-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b695d-112">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -IsAdmin
```

<span data-ttu-id="b695d-113">Bu komut, ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' parmak izine sahip sertifikayı kümeye ekler; böylece istemci kümeyle iletişim kurmak için sertifikayı yönetici olarak kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="b695d-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="b695d-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b695d-114">Example 2</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="b695d-115">Bu komut, ortak adı salt okunur bir istemci sertifikası ekler ' Contoso.com ' ve Issuer parmak izi ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A '.</span><span class="sxs-lookup"><span data-stu-id="b695d-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="b695d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b695d-116">PARAMETERS</span></span>

### <span data-ttu-id="b695d-117">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="b695d-117">-Admin</span></span>
<span data-ttu-id="b695d-118">İstemci kimlik doğrulama türü.</span><span class="sxs-lookup"><span data-stu-id="b695d-118">Client authentication type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b695d-119">-Adminclientparmak Izi</span><span class="sxs-lookup"><span data-stu-id="b695d-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="b695d-120">Yalnızca yönetici izni olan istemci sertifikası parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b695d-120">Specify client certificate thumbprint that only has admin permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b695d-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="b695d-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="b695d-122">İstemci ortak adını, verenin parmak izini ve kimlik doğrulama türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="b695d-122">Specify client common name, issuer thumbprint, and authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b695d-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="b695d-123">-CommonName</span></span>
<span data-ttu-id="b695d-124">İstemci sertifikası ortak adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b695d-124">Specify client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b695d-125">-Issuerparmak Izi</span><span class="sxs-lookup"><span data-stu-id="b695d-125">-IssuerThumbprint</span></span>
<span data-ttu-id="b695d-126">İstemci sertifikası verenin parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b695d-126">Specify client certificate issuer thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b695d-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="b695d-127">-Name</span></span>
<span data-ttu-id="b695d-128">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b695d-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b695d-129">-Readonlyclientparmak Izi</span><span class="sxs-lookup"><span data-stu-id="b695d-129">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="b695d-130">Salt okunur izni olan istemci sertifikası parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b695d-130">Specify client certificate thumbprint that has read only permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b695d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b695d-131">-ResourceGroupName</span></span>
<span data-ttu-id="b695d-132">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b695d-132">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b695d-133">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="b695d-133">-Thumbprint</span></span>
<span data-ttu-id="b695d-134">İstemci sertifikası parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b695d-134">Specify client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b695d-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="b695d-135">-Confirm</span></span>
<span data-ttu-id="b695d-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b695d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b695d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b695d-137">-WhatIf</span></span>
<span data-ttu-id="b695d-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b695d-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b695d-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b695d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b695d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b695d-140">-DefaultProfile</span></span>
<span data-ttu-id="b695d-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b695d-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b695d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b695d-142">CommonParameters</span></span>
<span data-ttu-id="b695d-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b695d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b695d-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b695d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b695d-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b695d-145">INPUTS</span></span>

### <span data-ttu-id="b695d-146">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b695d-146">System.Collections.Hashtable</span></span>
<span data-ttu-id="b695d-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b695d-147">System.String</span></span>

<span data-ttu-id="b695d-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b695d-148">System.Boolean</span></span>

## <span data-ttu-id="b695d-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b695d-149">OUTPUTS</span></span>

### <span data-ttu-id="b695d-150">Microsoft. Azure. Commands. ServiceFabric. modeller. PsCluster</span><span class="sxs-lookup"><span data-stu-id="b695d-150">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="b695d-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b695d-151">NOTES</span></span>

## <span data-ttu-id="b695d-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b695d-152">RELATED LINKS</span></span>

[<span data-ttu-id="b695d-153">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b695d-153">Remove-AzureRmServiceFabricClientCertificate</span></span>](./Remove-AzureRmServiceFabricClientCertificate.md)
