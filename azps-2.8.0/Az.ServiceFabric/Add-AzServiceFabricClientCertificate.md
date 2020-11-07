---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: de43485cc4504d8819e16e121bb94a29ae6b650a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932439"
---
# <span data-ttu-id="e9f08-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e9f08-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="e9f08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9f08-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f08-103">İstemci kimlik doğrulama amaçları için kümeye ortak ad veya parmak izi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e9f08-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="e9f08-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9f08-104">SYNTAX</span></span>

### <span data-ttu-id="e9f08-105">Singleupdatewithparmak Izi</span><span class="sxs-lookup"><span data-stu-id="e9f08-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9f08-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="e9f08-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9f08-107">Multipleupdateswithname</span><span class="sxs-lookup"><span data-stu-id="e9f08-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9f08-108">Çoğulgüncelleştirmeleriwithparmak Izi</span><span class="sxs-lookup"><span data-stu-id="e9f08-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9f08-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9f08-109">DESCRIPTION</span></span>
<span data-ttu-id="e9f08-110">Bir ortak ad ve veren parmak izi veya sertifika parmak izi eklemek için **Add-AzServiceFabricClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="e9f08-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="e9f08-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9f08-111">EXAMPLES</span></span>

### <span data-ttu-id="e9f08-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e9f08-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="e9f08-113">Bu komut, ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' parmak izine sahip sertifikayı kümeye ekler; böylece istemci kümeyle iletişim kurmak için sertifikayı yönetici olarak kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="e9f08-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="e9f08-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e9f08-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="e9f08-115">Bu komut, ortak adı salt okunur bir istemci sertifikası ekler ' Contoso.com ' ve Issuer parmak izi ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A '.</span><span class="sxs-lookup"><span data-stu-id="e9f08-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="e9f08-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9f08-116">PARAMETERS</span></span>

### <span data-ttu-id="e9f08-117">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="e9f08-117">-Admin</span></span>
<span data-ttu-id="e9f08-118">İstemci kimlik doğrulama türü</span><span class="sxs-lookup"><span data-stu-id="e9f08-118">Client authentication type</span></span>

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

### <span data-ttu-id="e9f08-119">-Adminclientparmak Izi</span><span class="sxs-lookup"><span data-stu-id="e9f08-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="e9f08-120">Yalnızca yönetici izni olan istemci sertifikası parmak izini belirtme</span><span class="sxs-lookup"><span data-stu-id="e9f08-120">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="e9f08-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="e9f08-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="e9f08-122">İstemci ortak adını, verenin parmak izini ve kimlik doğrulama türünü belirtme</span><span class="sxs-lookup"><span data-stu-id="e9f08-122">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="e9f08-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="e9f08-123">-CommonName</span></span>
<span data-ttu-id="e9f08-124">İstemci sertifikası ortak adını belirtme</span><span class="sxs-lookup"><span data-stu-id="e9f08-124">Specify client certificate common name</span></span>

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

### <span data-ttu-id="e9f08-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f08-125">-DefaultProfile</span></span>
<span data-ttu-id="e9f08-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e9f08-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9f08-127">-Issuerparmak Izi</span><span class="sxs-lookup"><span data-stu-id="e9f08-127">-IssuerThumbprint</span></span>
<span data-ttu-id="e9f08-128">İstemci sertifikasının verenin parmak izini belirtme</span><span class="sxs-lookup"><span data-stu-id="e9f08-128">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="e9f08-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="e9f08-129">-Name</span></span>
<span data-ttu-id="e9f08-130">Kümenin adını belirtme</span><span class="sxs-lookup"><span data-stu-id="e9f08-130">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="e9f08-131">-Readonlyclientparmak Izi</span><span class="sxs-lookup"><span data-stu-id="e9f08-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="e9f08-132">Yalnızca salt okunur izni olan istemci sertifikası parmak izini belirtme</span><span class="sxs-lookup"><span data-stu-id="e9f08-132">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="e9f08-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9f08-133">-ResourceGroupName</span></span>
<span data-ttu-id="e9f08-134">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="e9f08-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e9f08-135">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="e9f08-135">-Thumbprint</span></span>
<span data-ttu-id="e9f08-136">İstemci sertifikası parmak izini belirtme</span><span class="sxs-lookup"><span data-stu-id="e9f08-136">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="e9f08-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="e9f08-137">-Confirm</span></span>
<span data-ttu-id="e9f08-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e9f08-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9f08-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9f08-139">-WhatIf</span></span>
<span data-ttu-id="e9f08-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9f08-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9f08-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e9f08-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9f08-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f08-142">CommonParameters</span></span>
<span data-ttu-id="e9f08-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9f08-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f08-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9f08-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f08-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9f08-145">INPUTS</span></span>

### <span data-ttu-id="e9f08-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e9f08-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e9f08-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e9f08-147">System.String</span></span>

### <span data-ttu-id="e9f08-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="e9f08-148">System.String[]</span></span>

### <span data-ttu-id="e9f08-149">Microsoft. Azure. Commands. ServiceFabric. modeller. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="e9f08-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="e9f08-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9f08-150">OUTPUTS</span></span>

### <span data-ttu-id="e9f08-151">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="e9f08-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="e9f08-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9f08-152">NOTES</span></span>

## <span data-ttu-id="e9f08-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9f08-153">RELATED LINKS</span></span>

[<span data-ttu-id="e9f08-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e9f08-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
