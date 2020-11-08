---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: 913b610bc1d79c7a1792c06b53947fd3bf51151a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096351"
---
# <span data-ttu-id="39eba-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="39eba-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="39eba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39eba-102">SYNOPSIS</span></span>
<span data-ttu-id="39eba-103">İstemci kimlik doğrulama amaçları için kümeye ortak ad veya parmak izi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="39eba-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="39eba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39eba-104">SYNTAX</span></span>

### <span data-ttu-id="39eba-105">Singleupdatewithparmak Izi</span><span class="sxs-lookup"><span data-stu-id="39eba-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39eba-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="39eba-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39eba-107">Multipleupdateswithname</span><span class="sxs-lookup"><span data-stu-id="39eba-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39eba-108">Çoğulgüncelleştirmeleriwithparmak Izi</span><span class="sxs-lookup"><span data-stu-id="39eba-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39eba-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="39eba-109">DESCRIPTION</span></span>
<span data-ttu-id="39eba-110">Bir ortak ad ve veren parmak izi veya sertifika parmak izi eklemek için **Add-AzServiceFabricClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="39eba-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="39eba-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39eba-111">EXAMPLES</span></span>

### <span data-ttu-id="39eba-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="39eba-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="39eba-113">Bu komut, ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' parmak izine sahip sertifikayı kümeye ekler; böylece istemci kümeyle iletişim kurmak için sertifikayı yönetici olarak kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="39eba-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="39eba-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="39eba-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="39eba-115">Bu komut, ortak adı salt okunur bir istemci sertifikası ekler ' Contoso.com ' ve Issuer parmak izi ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A '.</span><span class="sxs-lookup"><span data-stu-id="39eba-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="39eba-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39eba-116">PARAMETERS</span></span>

### <span data-ttu-id="39eba-117">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="39eba-117">-Admin</span></span>
<span data-ttu-id="39eba-118">İstemci kimlik doğrulama türü</span><span class="sxs-lookup"><span data-stu-id="39eba-118">Client authentication type</span></span>

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

### <span data-ttu-id="39eba-119">-Adminclientparmak Izi</span><span class="sxs-lookup"><span data-stu-id="39eba-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="39eba-120">Yalnızca yönetici izni olan istemci sertifikası parmak izini belirtme</span><span class="sxs-lookup"><span data-stu-id="39eba-120">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="39eba-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="39eba-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="39eba-122">İstemci ortak adını, verenin parmak izini ve kimlik doğrulama türünü belirtme</span><span class="sxs-lookup"><span data-stu-id="39eba-122">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="39eba-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="39eba-123">-CommonName</span></span>
<span data-ttu-id="39eba-124">İstemci sertifikası ortak adını belirtme</span><span class="sxs-lookup"><span data-stu-id="39eba-124">Specify client certificate common name</span></span>

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

### <span data-ttu-id="39eba-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39eba-125">-DefaultProfile</span></span>
<span data-ttu-id="39eba-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="39eba-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39eba-127">-Issuerparmak Izi</span><span class="sxs-lookup"><span data-stu-id="39eba-127">-IssuerThumbprint</span></span>
<span data-ttu-id="39eba-128">İstemci sertifikasının verenin parmak izini belirtme</span><span class="sxs-lookup"><span data-stu-id="39eba-128">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="39eba-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="39eba-129">-Name</span></span>
<span data-ttu-id="39eba-130">Kümenin adını belirtme</span><span class="sxs-lookup"><span data-stu-id="39eba-130">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="39eba-131">-Readonlyclientparmak Izi</span><span class="sxs-lookup"><span data-stu-id="39eba-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="39eba-132">Yalnızca salt okunur izni olan istemci sertifikası parmak izini belirtme</span><span class="sxs-lookup"><span data-stu-id="39eba-132">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="39eba-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39eba-133">-ResourceGroupName</span></span>
<span data-ttu-id="39eba-134">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="39eba-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="39eba-135">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="39eba-135">-Thumbprint</span></span>
<span data-ttu-id="39eba-136">İstemci sertifikası parmak izini belirtme</span><span class="sxs-lookup"><span data-stu-id="39eba-136">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="39eba-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="39eba-137">-Confirm</span></span>
<span data-ttu-id="39eba-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="39eba-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39eba-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39eba-139">-WhatIf</span></span>
<span data-ttu-id="39eba-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="39eba-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39eba-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="39eba-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39eba-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39eba-142">CommonParameters</span></span>
<span data-ttu-id="39eba-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39eba-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39eba-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39eba-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39eba-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39eba-145">INPUTS</span></span>

### <span data-ttu-id="39eba-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="39eba-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="39eba-147">System. String</span><span class="sxs-lookup"><span data-stu-id="39eba-147">System.String</span></span>

### <span data-ttu-id="39eba-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="39eba-148">System.String[]</span></span>

### <span data-ttu-id="39eba-149">Microsoft. Azure. Commands. ServiceFabric. modeller. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="39eba-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="39eba-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39eba-150">OUTPUTS</span></span>

### <span data-ttu-id="39eba-151">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="39eba-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="39eba-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39eba-152">NOTES</span></span>

## <span data-ttu-id="39eba-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39eba-153">RELATED LINKS</span></span>

[<span data-ttu-id="39eba-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="39eba-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)