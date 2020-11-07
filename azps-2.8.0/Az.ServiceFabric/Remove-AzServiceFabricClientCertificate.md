---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: d2488792b5893e3972aa27ce98f87a23cec23073
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932423"
---
# <span data-ttu-id="1af07-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1af07-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="1af07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1af07-102">SYNOPSIS</span></span>
<span data-ttu-id="1af07-103">İstemci kimlik doğrulaması için kullanılan istemci sertifikasını veya sertifika konu adlarını (s) kümeye kaldırın.</span><span class="sxs-lookup"><span data-stu-id="1af07-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="1af07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1af07-104">SYNTAX</span></span>

### <span data-ttu-id="1af07-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="1af07-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1af07-106">Singleupdatewithparmak Izi</span><span class="sxs-lookup"><span data-stu-id="1af07-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1af07-107">Multipleupdateswithname</span><span class="sxs-lookup"><span data-stu-id="1af07-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1af07-108">Çoğulgüncelleştirmeleriwithparmak Izi</span><span class="sxs-lookup"><span data-stu-id="1af07-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1af07-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="1af07-109">DESCRIPTION</span></span>
<span data-ttu-id="1af07-110">Bir istemci sertifikasını (s) veya sertifika konu adlarını (s) kümede istemci kimlik doğrulaması için kullanılan şekilde kaldırmak için **Remove-AzServiceFabricClientCertificate** öğesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1af07-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="1af07-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1af07-111">EXAMPLES</span></span>

### <span data-ttu-id="1af07-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1af07-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="1af07-113">Bu komut, ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' parmak izine sahip istemci sertifikasını kümeden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1af07-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="1af07-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1af07-114">PARAMETERS</span></span>

### <span data-ttu-id="1af07-115">-Adminclientparmak Izi</span><span class="sxs-lookup"><span data-stu-id="1af07-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="1af07-116">Yalnızca yönetici izni olan istemci sertifikası parmak izini belirtme</span><span class="sxs-lookup"><span data-stu-id="1af07-116">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="1af07-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="1af07-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="1af07-118">İstemci ortak adını, verenin parmak izini ve kimlik doğrulama türünü belirtme</span><span class="sxs-lookup"><span data-stu-id="1af07-118">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="1af07-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="1af07-119">-CommonName</span></span>
<span data-ttu-id="1af07-120">İstemci sertifikası ortak adını belirtme</span><span class="sxs-lookup"><span data-stu-id="1af07-120">Specify client certificate common name</span></span>

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

### <span data-ttu-id="1af07-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af07-121">-DefaultProfile</span></span>
<span data-ttu-id="1af07-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1af07-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1af07-123">-Issuerparmak Izi</span><span class="sxs-lookup"><span data-stu-id="1af07-123">-IssuerThumbprint</span></span>
<span data-ttu-id="1af07-124">İstemci sertifikasının verenin parmak izini belirtme</span><span class="sxs-lookup"><span data-stu-id="1af07-124">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="1af07-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="1af07-125">-Name</span></span>
<span data-ttu-id="1af07-126">Kümenin adını belirtme</span><span class="sxs-lookup"><span data-stu-id="1af07-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="1af07-127">-Readonlyclientparmak Izi</span><span class="sxs-lookup"><span data-stu-id="1af07-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="1af07-128">Yalnızca salt okunur izni olan istemci sertifikası parmak izini belirtme</span><span class="sxs-lookup"><span data-stu-id="1af07-128">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="1af07-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af07-129">-ResourceGroupName</span></span>
<span data-ttu-id="1af07-130">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1af07-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1af07-131">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="1af07-131">-Thumbprint</span></span>
<span data-ttu-id="1af07-132">İstemci sertifikası parmak izini belirtme</span><span class="sxs-lookup"><span data-stu-id="1af07-132">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="1af07-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="1af07-133">-Confirm</span></span>
<span data-ttu-id="1af07-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1af07-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1af07-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1af07-135">-WhatIf</span></span>
<span data-ttu-id="1af07-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1af07-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1af07-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1af07-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1af07-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af07-138">CommonParameters</span></span>
<span data-ttu-id="1af07-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1af07-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af07-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1af07-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af07-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1af07-141">INPUTS</span></span>

### <span data-ttu-id="1af07-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1af07-142">System.String</span></span>

### <span data-ttu-id="1af07-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="1af07-143">System.String[]</span></span>

### <span data-ttu-id="1af07-144">Microsoft. Azure. Commands. ServiceFabric. modeller. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="1af07-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="1af07-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1af07-145">OUTPUTS</span></span>

### <span data-ttu-id="1af07-146">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="1af07-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="1af07-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1af07-147">NOTES</span></span>

## <span data-ttu-id="1af07-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1af07-148">RELATED LINKS</span></span>

[<span data-ttu-id="1af07-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1af07-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
