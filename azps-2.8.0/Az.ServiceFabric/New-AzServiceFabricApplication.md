---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: 7a337ed6e347d5ab22cd04baac2acb1c7e0b171d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933194"
---
# <span data-ttu-id="2d2d3-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2d2d3-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="2d2d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d2d3-102">SYNOPSIS</span></span>
<span data-ttu-id="2d2d3-103">Belirtilen kaynak grubu ve küme altında yeni hizmet dokusu uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="2d2d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d2d3-104">SYNTAX</span></span>

### <span data-ttu-id="2d2d3-105">SkipAppTypeVersion (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2d2d3-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d2d3-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2d2d3-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d2d3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d2d3-107">DESCRIPTION</span></span>
<span data-ttu-id="2d2d3-108">Bu cmdlet, belirtilen kaynak grubu ve küme altında yeni bir hizmet yapısı uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="2d2d3-109">Tür sürümü ' başarısız ' durumunda olduğunda, tür sürümünü oluşturmak için parametre-PackageUrl 'Si kullanılabilir ancak ' başarısız ' durumunda cmdlet kullanıcının tür sürümünü yeniden oluşturmak isteyip istemediğini sorar.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="2d2d3-110">' Başarısız ' durumunda devam ederse komut işlemi durdurur ve bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="2d2d3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d2d3-111">EXAMPLES</span></span>

### <span data-ttu-id="2d2d3-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2d2d3-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="2d2d3-113">Bu örnek, kaynak grubu "testRG" ve Cluster "testCluster" altındaki "testApp" uygulamasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="2d2d3-114">"TestAppType" sürümü "v1" uygulama türü zaten kümede var olmalıdır ve uygulama bildiriminde uygulama parametreleri de tanımlanmalıdır; Aksi halde cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="2d2d3-115">Örnek 2: uygulamayı oluşturmadan önce uygulama türü sürümünü oluşturmak için-PackageUrl belirtin.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="2d2d3-116">Bu örnek, sağlanan Package URL 'sini kullanarak "TestAppType" sürüm "v1" uygulama türü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="2d2d3-117">Bundan sonra, uygulamayı oluşturmak için normal süreç devam edecektir.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="2d2d3-118">Uygulama türü sürümü varsa ve sağlama durumu ' başarısız oldu ' olarak, kullanıcının tür sürümünü yeniden oluşturmak isteyip istemediğini karar versin.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="2d2d3-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d2d3-119">PARAMETERS</span></span>

### <span data-ttu-id="2d2d3-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="2d2d3-120">-ApplicationParameter</span></span>
<span data-ttu-id="2d2d3-121">Uygulama parametrelerini anahtar/değer çiftleri olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="2d2d3-122">Bu parametreler uygulama bildiriminde bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-122">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="2d2d3-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="2d2d3-123">-ApplicationTypeName</span></span>
<span data-ttu-id="2d2d3-124">Uygulama türünün adını belirtme</span><span class="sxs-lookup"><span data-stu-id="2d2d3-124">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2d3-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2d2d3-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="2d2d3-126">Uygulama türü sürümünü belirtme</span><span class="sxs-lookup"><span data-stu-id="2d2d3-126">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2d3-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2d2d3-127">-ClusterName</span></span>
<span data-ttu-id="2d2d3-128">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2d2d3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d2d3-129">-DefaultProfile</span></span>
<span data-ttu-id="2d2d3-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d2d3-131">-Force</span><span class="sxs-lookup"><span data-stu-id="2d2d3-131">-Force</span></span>
<span data-ttu-id="2d2d3-132">Sormadan devam et</span><span class="sxs-lookup"><span data-stu-id="2d2d3-132">Continue without prompts</span></span>

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

### <span data-ttu-id="2d2d3-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="2d2d3-133">-MaximumNodeCount</span></span>
<span data-ttu-id="2d2d3-134">Uygulamanın yerleştirileceği en fazla düğüm sayısını belirtir</span><span class="sxs-lookup"><span data-stu-id="2d2d3-134">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2d3-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="2d2d3-135">-MinimumNodeCount</span></span>
<span data-ttu-id="2d2d3-136">Bu uygulama için hizmet yapınızın kapasiteyi ayırabileceği en az düğüm sayısını belirtir</span><span class="sxs-lookup"><span data-stu-id="2d2d3-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2d3-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="2d2d3-137">-Name</span></span>
<span data-ttu-id="2d2d3-138">Uygulamanın adını belirtme</span><span class="sxs-lookup"><span data-stu-id="2d2d3-138">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2d3-139">-PackageUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="2d2d3-139">-PackageUrl</span></span>
<span data-ttu-id="2d2d3-140">Uygulama paketinin URL 'sini belirtme</span><span class="sxs-lookup"><span data-stu-id="2d2d3-140">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAppTypeVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d2d3-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d2d3-141">-ResourceGroupName</span></span>
<span data-ttu-id="2d2d3-142">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2d2d3-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="2d2d3-143">-Confirm</span></span>
<span data-ttu-id="2d2d3-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d2d3-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d2d3-145">-WhatIf</span></span>
<span data-ttu-id="2d2d3-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d2d3-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d2d3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d2d3-148">CommonParameters</span></span>
<span data-ttu-id="2d2d3-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d2d3-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d2d3-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d2d3-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d2d3-151">INPUTS</span></span>

### <span data-ttu-id="2d2d3-152">System. String</span><span class="sxs-lookup"><span data-stu-id="2d2d3-152">System.String</span></span>

### <span data-ttu-id="2d2d3-153">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2d2d3-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2d2d3-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d2d3-154">OUTPUTS</span></span>

### <span data-ttu-id="2d2d3-155">Microsoft. Azure. Commands. ServiceFabric. modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="2d2d3-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="2d2d3-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d2d3-156">NOTES</span></span>

## <span data-ttu-id="2d2d3-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d2d3-157">RELATED LINKS</span></span>