---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: dc9f7dfa26b350a5dadea4bfa3afb9ad832fa063
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097157"
---
# <span data-ttu-id="0b4f1-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0b4f1-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="0b4f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b4f1-102">SYNOPSIS</span></span>
<span data-ttu-id="0b4f1-103">İstemci kimlik doğrulaması için kullanılan istemci sertifikasını veya sertifika konu adlarını (s) kümeye kaldırın.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="0b4f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b4f1-104">SYNTAX</span></span>

### <span data-ttu-id="0b4f1-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="0b4f1-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b4f1-106">Singleupdatewithparmak Izi</span><span class="sxs-lookup"><span data-stu-id="0b4f1-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b4f1-107">Multipleupdateswithname</span><span class="sxs-lookup"><span data-stu-id="0b4f1-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b4f1-108">Çoğulgüncelleştirmeleriwithparmak Izi</span><span class="sxs-lookup"><span data-stu-id="0b4f1-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b4f1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b4f1-109">DESCRIPTION</span></span>
<span data-ttu-id="0b4f1-110">Bir istemci sertifikasını (s) veya sertifika konu adlarını (s) kümede istemci kimlik doğrulaması için kullanılan şekilde kaldırmak için **Remove-AzServiceFabricClientCertificate** öğesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="0b4f1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b4f1-111">EXAMPLES</span></span>

### <span data-ttu-id="0b4f1-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0b4f1-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="0b4f1-113">Bu komut, ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' parmak izine sahip istemci sertifikasını kümeden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="0b4f1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b4f1-114">PARAMETERS</span></span>

### <span data-ttu-id="0b4f1-115">-Adminclientparmak Izi</span><span class="sxs-lookup"><span data-stu-id="0b4f1-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="0b4f1-116">Yalnızca yönetici izni olan istemci sertifikası parmak izini belirtme</span><span class="sxs-lookup"><span data-stu-id="0b4f1-116">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="0b4f1-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="0b4f1-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="0b4f1-118">İstemci ortak adını, verenin parmak izini ve kimlik doğrulama türünü belirtme</span><span class="sxs-lookup"><span data-stu-id="0b4f1-118">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="0b4f1-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="0b4f1-119">-CommonName</span></span>
<span data-ttu-id="0b4f1-120">İstemci sertifikası ortak adını belirtme</span><span class="sxs-lookup"><span data-stu-id="0b4f1-120">Specify client certificate common name</span></span>

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

### <span data-ttu-id="0b4f1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b4f1-121">-DefaultProfile</span></span>
<span data-ttu-id="0b4f1-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b4f1-123">-Issuerparmak Izi</span><span class="sxs-lookup"><span data-stu-id="0b4f1-123">-IssuerThumbprint</span></span>
<span data-ttu-id="0b4f1-124">İstemci sertifikasının verenin parmak izini belirtme</span><span class="sxs-lookup"><span data-stu-id="0b4f1-124">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="0b4f1-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b4f1-125">-Name</span></span>
<span data-ttu-id="0b4f1-126">Kümenin adını belirtme</span><span class="sxs-lookup"><span data-stu-id="0b4f1-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="0b4f1-127">-Readonlyclientparmak Izi</span><span class="sxs-lookup"><span data-stu-id="0b4f1-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="0b4f1-128">Yalnızca salt okunur izni olan istemci sertifikası parmak izini belirtme</span><span class="sxs-lookup"><span data-stu-id="0b4f1-128">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="0b4f1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b4f1-129">-ResourceGroupName</span></span>
<span data-ttu-id="0b4f1-130">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0b4f1-131">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="0b4f1-131">-Thumbprint</span></span>
<span data-ttu-id="0b4f1-132">İstemci sertifikası parmak izini belirtme</span><span class="sxs-lookup"><span data-stu-id="0b4f1-132">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="0b4f1-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b4f1-133">-Confirm</span></span>
<span data-ttu-id="0b4f1-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b4f1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b4f1-135">-WhatIf</span></span>
<span data-ttu-id="0b4f1-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b4f1-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b4f1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b4f1-138">CommonParameters</span></span>
<span data-ttu-id="0b4f1-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b4f1-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b4f1-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b4f1-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b4f1-141">INPUTS</span></span>

### <span data-ttu-id="0b4f1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0b4f1-142">System.String</span></span>

### <span data-ttu-id="0b4f1-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="0b4f1-143">System.String[]</span></span>

### <span data-ttu-id="0b4f1-144">Microsoft. Azure. Commands. ServiceFabric. modeller. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="0b4f1-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="0b4f1-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b4f1-145">OUTPUTS</span></span>

### <span data-ttu-id="0b4f1-146">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="0b4f1-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="0b4f1-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b4f1-147">NOTES</span></span>

## <span data-ttu-id="0b4f1-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b4f1-148">RELATED LINKS</span></span>

[<span data-ttu-id="0b4f1-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0b4f1-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
