---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: e508afc5ab66a3e2aec49131bf2c8bf0e9d31259
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762353"
---
# <span data-ttu-id="38e98-101">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="38e98-101">Remove-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="38e98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38e98-102">SYNOPSIS</span></span>
<span data-ttu-id="38e98-103">İstemci kimlik doğrulaması için kullanılan istemci sertifikasını veya sertifika konu adlarını (s) kümeye kaldırın.</span><span class="sxs-lookup"><span data-stu-id="38e98-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38e98-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38e98-104">SYNTAX</span></span>

### <span data-ttu-id="38e98-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="38e98-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38e98-106">Singleupdatewithparmak Izi</span><span class="sxs-lookup"><span data-stu-id="38e98-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38e98-107">Multipleupdateswithname</span><span class="sxs-lookup"><span data-stu-id="38e98-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38e98-108">Çoğulgüncelleştirmeleriwithparmak Izi</span><span class="sxs-lookup"><span data-stu-id="38e98-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38e98-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="38e98-109">DESCRIPTION</span></span>
<span data-ttu-id="38e98-110">Bir istemci sertifikasını (s) veya sertifika konu adlarını (s) kümede istemci kimlik doğrulaması için kullanılmasını kaldırmak için **Remove-AzureRmServiceFabricClientCertificate** öğesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="38e98-110">Use **Remove-AzureRmServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="38e98-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38e98-111">EXAMPLES</span></span>

### <span data-ttu-id="38e98-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="38e98-112">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="38e98-113">Bu komut, ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' parmak izine sahip istemci sertifikasını kümeden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="38e98-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="38e98-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38e98-114">PARAMETERS</span></span>

### <span data-ttu-id="38e98-115">-Adminclientparmak Izi</span><span class="sxs-lookup"><span data-stu-id="38e98-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="38e98-116">Yalnızca yönetici izni olan istemci sertifikası parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="38e98-116">Specify client certificate thumbprint that only has admin permission.</span></span>

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

### <span data-ttu-id="38e98-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="38e98-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="38e98-118">İstemci ortak adını, verenin parmak izini ve kimlik doğrulama türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="38e98-118">Specify client common name, issuer thumbprint, and authentication type.</span></span>

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

### <span data-ttu-id="38e98-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="38e98-119">-CommonName</span></span>
<span data-ttu-id="38e98-120">İstemci sertifikası ortak adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="38e98-120">Specify client certificate common name.</span></span>

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

### <span data-ttu-id="38e98-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38e98-121">-DefaultProfile</span></span>
<span data-ttu-id="38e98-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="38e98-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38e98-123">-Issuerparmak Izi</span><span class="sxs-lookup"><span data-stu-id="38e98-123">-IssuerThumbprint</span></span>
<span data-ttu-id="38e98-124">İstemci sertifikası verenin parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="38e98-124">Specify client certificate issuer thumbprint.</span></span>

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

### <span data-ttu-id="38e98-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="38e98-125">-Name</span></span>
<span data-ttu-id="38e98-126">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="38e98-126">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="38e98-127">-Readonlyclientparmak Izi</span><span class="sxs-lookup"><span data-stu-id="38e98-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="38e98-128">Salt okunur izni olan istemci sertifikası parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="38e98-128">Specify client certificate thumbprint that has read only permission.</span></span>

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

### <span data-ttu-id="38e98-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38e98-129">-ResourceGroupName</span></span>
<span data-ttu-id="38e98-130">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38e98-130">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="38e98-131">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="38e98-131">-Thumbprint</span></span>
<span data-ttu-id="38e98-132">İstemci sertifikası parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="38e98-132">Specify client certificate thumbprint.</span></span>

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

### <span data-ttu-id="38e98-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="38e98-133">-Confirm</span></span>
<span data-ttu-id="38e98-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="38e98-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38e98-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38e98-135">-WhatIf</span></span>
<span data-ttu-id="38e98-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="38e98-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38e98-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="38e98-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38e98-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38e98-138">CommonParameters</span></span>
<span data-ttu-id="38e98-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38e98-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38e98-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38e98-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38e98-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38e98-141">INPUTS</span></span>

### <span data-ttu-id="38e98-142">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="38e98-142">System.Collections.Hashtable</span></span>
<span data-ttu-id="38e98-143">System. String</span><span class="sxs-lookup"><span data-stu-id="38e98-143">System.String</span></span>

<span data-ttu-id="38e98-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="38e98-144">System.Boolean</span></span>

## <span data-ttu-id="38e98-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38e98-145">OUTPUTS</span></span>

### <span data-ttu-id="38e98-146">Microsoft. Azure. Commands. ServiceFabric. modeller. PsCluster</span><span class="sxs-lookup"><span data-stu-id="38e98-146">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="38e98-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38e98-147">NOTES</span></span>

## <span data-ttu-id="38e98-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38e98-148">RELATED LINKS</span></span>

[<span data-ttu-id="38e98-149">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="38e98-149">Add-AzureRmServiceFabricClientCertificate</span></span>](./Add-AzureRmServiceFabricClientCertificate.md)
