---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: 369c642485e3c83f4eaf6dee986beca676ea5051
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764116"
---
# <span data-ttu-id="d0f9e-101">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d0f9e-101">Remove-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="d0f9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0f9e-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f9e-103">İstemci kimlik doğrulaması için kullanılan istemci sertifikasını veya sertifika konu adlarını (s) kümeye kaldırın.</span><span class="sxs-lookup"><span data-stu-id="d0f9e-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0f9e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d0f9e-104">SYNTAX</span></span>

### <span data-ttu-id="d0f9e-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="d0f9e-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0f9e-106">Singleupdatewithparmak Izi</span><span class="sxs-lookup"><span data-stu-id="d0f9e-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0f9e-107">Multipleupdateswithname</span><span class="sxs-lookup"><span data-stu-id="d0f9e-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0f9e-108">Çoğulgüncelleştirmeleriwithparmak Izi</span><span class="sxs-lookup"><span data-stu-id="d0f9e-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0f9e-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0f9e-109">DESCRIPTION</span></span>
<span data-ttu-id="d0f9e-110">Bir istemci sertifikasını (s) veya sertifika konu adlarını (s) kümede istemci kimlik doğrulaması için kullanılmasını kaldırmak için **Remove-AzureRmServiceFabricClientCertificate** öğesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d0f9e-110">Use **Remove-AzureRmServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="d0f9e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d0f9e-111">EXAMPLES</span></span>

### <span data-ttu-id="d0f9e-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d0f9e-112">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="d0f9e-113">Bu komut, ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' parmak izine sahip istemci sertifikasını kümeden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d0f9e-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="d0f9e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d0f9e-114">PARAMETERS</span></span>

### <span data-ttu-id="d0f9e-115">-Adminclientparmak Izi</span><span class="sxs-lookup"><span data-stu-id="d0f9e-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="d0f9e-116">Yalnızca yönetici izni olan istemci sertifikası parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d0f9e-116">Specify client certificate thumbprint that only has admin permission.</span></span>

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

### <span data-ttu-id="d0f9e-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="d0f9e-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="d0f9e-118">İstemci ortak adını, verenin parmak izini ve kimlik doğrulama türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="d0f9e-118">Specify client common name, issuer thumbprint, and authentication type.</span></span>

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

### <span data-ttu-id="d0f9e-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="d0f9e-119">-CommonName</span></span>
<span data-ttu-id="d0f9e-120">İstemci sertifikası ortak adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d0f9e-120">Specify client certificate common name.</span></span>

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

### <span data-ttu-id="d0f9e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f9e-121">-DefaultProfile</span></span>
<span data-ttu-id="d0f9e-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d0f9e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0f9e-123">-Issuerparmak Izi</span><span class="sxs-lookup"><span data-stu-id="d0f9e-123">-IssuerThumbprint</span></span>
<span data-ttu-id="d0f9e-124">İstemci sertifikası verenin parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d0f9e-124">Specify client certificate issuer thumbprint.</span></span>

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

### <span data-ttu-id="d0f9e-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="d0f9e-125">-Name</span></span>
<span data-ttu-id="d0f9e-126">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d0f9e-126">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d0f9e-127">-Readonlyclientparmak Izi</span><span class="sxs-lookup"><span data-stu-id="d0f9e-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="d0f9e-128">Salt okunur izni olan istemci sertifikası parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d0f9e-128">Specify client certificate thumbprint that has read only permission.</span></span>

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

### <span data-ttu-id="d0f9e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0f9e-129">-ResourceGroupName</span></span>
<span data-ttu-id="d0f9e-130">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0f9e-130">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d0f9e-131">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="d0f9e-131">-Thumbprint</span></span>
<span data-ttu-id="d0f9e-132">İstemci sertifikası parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d0f9e-132">Specify client certificate thumbprint.</span></span>

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

### <span data-ttu-id="d0f9e-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="d0f9e-133">-Confirm</span></span>
<span data-ttu-id="d0f9e-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d0f9e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0f9e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0f9e-135">-WhatIf</span></span>
<span data-ttu-id="d0f9e-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d0f9e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0f9e-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d0f9e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0f9e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f9e-138">CommonParameters</span></span>
<span data-ttu-id="d0f9e-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d0f9e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f9e-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0f9e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f9e-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d0f9e-141">INPUTS</span></span>

### <span data-ttu-id="d0f9e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d0f9e-142">System.String</span></span>
<span data-ttu-id="d0f9e-143">Parametreler: CommonName (ByValue), ıssuerparmak Izi (ByValue), Parmak Izi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d0f9e-143">Parameters: CommonName (ByValue), IssuerThumbprint (ByValue), Thumbprint (ByValue)</span></span>

### <span data-ttu-id="d0f9e-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="d0f9e-144">System.String[]</span></span>
<span data-ttu-id="d0f9e-145">Parametreler: Adminclientparmak Izi (ByValue), Readonlyclientparmak Izi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d0f9e-145">Parameters: AdminClientThumbprint (ByValue), ReadonlyClientThumbprint (ByValue)</span></span>

### <span data-ttu-id="d0f9e-146">Microsoft. Azure. Commands. ServiceFabric. modeller. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="d0f9e-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>
<span data-ttu-id="d0f9e-147">Parametreler: ClientCertificateCommonName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d0f9e-147">Parameters: ClientCertificateCommonName (ByValue)</span></span>

## <span data-ttu-id="d0f9e-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d0f9e-148">OUTPUTS</span></span>

### <span data-ttu-id="d0f9e-149">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="d0f9e-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="d0f9e-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d0f9e-150">NOTES</span></span>

## <span data-ttu-id="d0f9e-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d0f9e-151">RELATED LINKS</span></span>

[<span data-ttu-id="d0f9e-152">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d0f9e-152">Add-AzureRmServiceFabricClientCertificate</span></span>](./Add-AzureRmServiceFabricClientCertificate.md)
