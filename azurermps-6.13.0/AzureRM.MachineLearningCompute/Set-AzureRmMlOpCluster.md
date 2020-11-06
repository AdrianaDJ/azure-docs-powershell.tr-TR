---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/set-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
ms.openlocfilehash: cbe72d14eac4864b784f31c4a800db09fc38b042
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590195"
---
# <span data-ttu-id="17610-101">Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="17610-101">Set-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="17610-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17610-102">SYNOPSIS</span></span>
<span data-ttu-id="17610-103">Bir operationalization kümesinin özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="17610-103">Sets the properties of an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17610-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17610-104">SYNTAX</span></span>

### <span data-ttu-id="17610-105">Setbybireyalparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="17610-105">SetByIndividualParameters (Default)</span></span>
```
Set-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17610-106">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="17610-106">SetByInputObject</span></span>
```
Set-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17610-107">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="17610-107">SetByResourceId</span></span>
```
Set-AzureRmMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17610-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="17610-108">DESCRIPTION</span></span>
<span data-ttu-id="17610-109">Bir operationalization kümesinin tüm özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="17610-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="17610-110">Küme nesnesini kullanırken tüm özellikleri ayarlarken tam olarak geçerli bir giriş nesnesi iletilmelidir.</span><span class="sxs-lookup"><span data-stu-id="17610-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="17610-111">Salt okunur özellikler yoksayılacak.</span><span class="sxs-lookup"><span data-stu-id="17610-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="17610-112">Parametre kümelerinde gösterildiği gibi, şu anda yalnızca bazı özellikler güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="17610-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="17610-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17610-113">EXAMPLES</span></span>

### <span data-ttu-id="17610-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="17610-114">Example 1</span></span>
<span data-ttu-id="17610-115">Tek tek parametreleri kullanarak kümeyi güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="17610-115">Update a cluster using individual parameters.</span></span>

```
PS C:\> Set-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="17610-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="17610-116">Example 2</span></span>
<span data-ttu-id="17610-117">Giriş nesnesini kullanarak kümeyi güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="17610-117">Update a cluster using an input object.</span></span>

```
PS C:\> $cluster = Get-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzureRmMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="17610-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17610-118">PARAMETERS</span></span>

### <span data-ttu-id="17610-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="17610-119">-AgentCount</span></span>
<span data-ttu-id="17610-120">ACS kümesindeki aracı düğümlerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="17610-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17610-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17610-121">-DefaultProfile</span></span>
<span data-ttu-id="17610-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="17610-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17610-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17610-123">-InputObject</span></span>
<span data-ttu-id="17610-124">Operationalization kümesi özellikleri.</span><span class="sxs-lookup"><span data-stu-id="17610-124">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17610-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="17610-125">-Name</span></span>
<span data-ttu-id="17610-126">Operationalization kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="17610-126">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17610-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17610-127">-ResourceGroupName</span></span>
<span data-ttu-id="17610-128">Operationalization kümesi için kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="17610-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17610-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="17610-129">-ResourceId</span></span>
<span data-ttu-id="17610-130">Operationalization kümesi için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="17610-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17610-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="17610-131">-SslCertificate</span></span>
<span data-ttu-id="17610-132">PEM biçimindeki SSL sertifikası verileri.</span><span class="sxs-lookup"><span data-stu-id="17610-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17610-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="17610-133">-SslCName</span></span>
<span data-ttu-id="17610-134">SSL sertifikası için CName.</span><span class="sxs-lookup"><span data-stu-id="17610-134">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17610-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="17610-135">-SslKey</span></span>
<span data-ttu-id="17610-136">PEM biçimindeki SSL anahtar verileri.</span><span class="sxs-lookup"><span data-stu-id="17610-136">The SSL key data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17610-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="17610-137">-SslStatus</span></span>
<span data-ttu-id="17610-138">SSL durumu.</span><span class="sxs-lookup"><span data-stu-id="17610-138">SSL status.</span></span>
<span data-ttu-id="17610-139">Olası değerler ' Enabled ' ve ' Disabled ' değerleridir.</span><span class="sxs-lookup"><span data-stu-id="17610-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17610-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="17610-140">-Confirm</span></span>
<span data-ttu-id="17610-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="17610-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17610-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17610-142">-WhatIf</span></span>
<span data-ttu-id="17610-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="17610-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17610-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="17610-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17610-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17610-145">CommonParameters</span></span>
<span data-ttu-id="17610-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17610-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17610-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17610-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17610-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17610-148">INPUTS</span></span>

### <span data-ttu-id="17610-149">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="17610-149">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="17610-150">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="17610-150">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="17610-151">System. String</span><span class="sxs-lookup"><span data-stu-id="17610-151">System.String</span></span>

### <span data-ttu-id="17610-152">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="17610-152">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="17610-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17610-153">OUTPUTS</span></span>

### <span data-ttu-id="17610-154">Microsoft. Azure. Commands. Machinon Arningcompute. model. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="17610-154">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="17610-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17610-155">NOTES</span></span>

## <span data-ttu-id="17610-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17610-156">RELATED LINKS</span></span>
