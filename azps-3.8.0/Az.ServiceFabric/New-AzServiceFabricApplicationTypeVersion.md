---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 69bbcbbd508a5bf32163b91378aab62dbdcb3a64
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097204"
---
# <span data-ttu-id="e173c-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e173c-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="e173c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e173c-102">SYNOPSIS</span></span>
<span data-ttu-id="e173c-103">Belirtilen kaynak grubu ve küme altında yeni uygulama türü sürümü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e173c-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="e173c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e173c-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e173c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e173c-105">DESCRIPTION</span></span>
<span data-ttu-id="e173c-106">Bu cmdlet, Package 'de belirtilen paketi kullanarak yeni bir uygulama türü sürümü oluşturur; Bu, dağıtım sırasında Azure Resource Manager için bir REST uç noktası aracılığıyla erişilebilir ve uygulamanın paketlenmesi</span><span class="sxs-lookup"><span data-stu-id="e173c-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="e173c-107">Bu komut zaten yoksa uygulama türü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e173c-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="e173c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e173c-108">EXAMPLES</span></span>

### <span data-ttu-id="e173c-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e173c-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="e173c-110">Bu örnek, "testAppType" türünde bir uygulama türü sürümü "v1" oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e173c-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="e173c-111">Pakette bulunan uygulama bildirimindeki sürüm, sürüm ile belirtilen sürümle aynı sürüme sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e173c-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="e173c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e173c-112">PARAMETERS</span></span>

### <span data-ttu-id="e173c-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e173c-113">-ClusterName</span></span>
<span data-ttu-id="e173c-114">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="e173c-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e173c-115">-DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="e173c-115">-DefaultParameter</span></span>
<span data-ttu-id="e173c-116">Uygulama parametrelerinin varsayılan değerlerini anahtar/değer çiftleri olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="e173c-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="e173c-117">Bu parametreler uygulama bildiriminde bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e173c-117">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e173c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e173c-118">-DefaultProfile</span></span>
<span data-ttu-id="e173c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e173c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e173c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e173c-120">-Force</span></span>
<span data-ttu-id="e173c-121">Sormadan devam et</span><span class="sxs-lookup"><span data-stu-id="e173c-121">Continue without prompts</span></span>

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

### <span data-ttu-id="e173c-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="e173c-122">-Name</span></span>
<span data-ttu-id="e173c-123">Uygulama türünün adını belirtme</span><span class="sxs-lookup"><span data-stu-id="e173c-123">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e173c-124">-PackageUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="e173c-124">-PackageUrl</span></span>
<span data-ttu-id="e173c-125">Uygulama paketinin URL 'sini belirtme</span><span class="sxs-lookup"><span data-stu-id="e173c-125">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e173c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e173c-126">-ResourceGroupName</span></span>
<span data-ttu-id="e173c-127">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="e173c-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e173c-128">-Version</span><span class="sxs-lookup"><span data-stu-id="e173c-128">-Version</span></span>
<span data-ttu-id="e173c-129">Uygulama türü sürümünü belirtme</span><span class="sxs-lookup"><span data-stu-id="e173c-129">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e173c-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="e173c-130">-Confirm</span></span>
<span data-ttu-id="e173c-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e173c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e173c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e173c-132">-WhatIf</span></span>
<span data-ttu-id="e173c-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e173c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e173c-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e173c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e173c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e173c-135">CommonParameters</span></span>
<span data-ttu-id="e173c-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e173c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e173c-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e173c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e173c-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e173c-138">INPUTS</span></span>

### <span data-ttu-id="e173c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e173c-139">System.String</span></span>

### <span data-ttu-id="e173c-140">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e173c-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e173c-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e173c-141">OUTPUTS</span></span>

### <span data-ttu-id="e173c-142">Microsoft. Azure. Commands. ServiceFabric. modeller. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e173c-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="e173c-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e173c-143">NOTES</span></span>

## <span data-ttu-id="e173c-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e173c-144">RELATED LINKS</span></span>
