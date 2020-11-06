---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 4cdc70928f2b27ae1e1604c52e5703798a302a66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593426"
---
# <span data-ttu-id="8a819-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8a819-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="8a819-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a819-102">SYNOPSIS</span></span>
<span data-ttu-id="8a819-103">Kaynak grubu dağıtımını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="8a819-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a819-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a819-104">SYNTAX</span></span>

### <span data-ttu-id="8a819-105">StopByResourceGroupDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8a819-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a819-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="8a819-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a819-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a819-107">DESCRIPTION</span></span>
<span data-ttu-id="8a819-108">**Stop-AzureRmResourceGroupDeployment** cmdlet 'i, başlatılmış ancak tamamlanmamış bir Azure Kaynak grubu dağıtımını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="8a819-108">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="8a819-109">Bir dağıtımı durdurmak için dağıtımın, sağlama gibi tamamlanmamış bir sağlama durumu olmalıdır; bunun sağlanması veya başarısız gibi tamamlanmamış bir durumda olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="8a819-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="8a819-110">Azure kaynağı, Web sitesi, veritabanı veya veritabanı sunucusu gibi kullanıcı tarafından yönetilen bir varlıktır.</span><span class="sxs-lookup"><span data-stu-id="8a819-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="8a819-111">Kaynak grubu, birim olarak dağıtılan kaynaklar topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="8a819-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="8a819-112">Kaynak grubu dağıtmak için New-AzureRmResourceGroupDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8a819-112">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>

<span data-ttu-id="8a819-113">New-AzureRmResource cmdlet 'i yeni bir kaynak oluşturur, ancak bu cmdlet 'in durdurmadığı bir kaynak grubu dağıtım işlemini tetiklemez.</span><span class="sxs-lookup"><span data-stu-id="8a819-113">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="8a819-114">Bu cmdlet yalnızca bir çalışan dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="8a819-114">This cmdlet stops only one running deployment.</span></span>

<span data-ttu-id="8a819-115">Belirli bir dağıtımı durdurmak için *Name* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8a819-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="8a819-116">*Name* parametresini atlarsanız, **stop-AzureRmResourceGroupDeployment** çalışan bir dağıtımı arar ve bunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="8a819-116">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="8a819-117">Cmdlet birden fazla çalışan dağıtım bulursa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="8a819-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="8a819-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a819-118">EXAMPLES</span></span>

## <span data-ttu-id="8a819-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a819-119">PARAMETERS</span></span>

### <span data-ttu-id="8a819-120">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="8a819-120">-ApiVersion</span></span>
<span data-ttu-id="8a819-121">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a819-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8a819-122">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8a819-122">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a819-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a819-123">-DefaultProfile</span></span>
<span data-ttu-id="8a819-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8a819-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a819-125">-ID</span><span class="sxs-lookup"><span data-stu-id="8a819-125">-Id</span></span>
<span data-ttu-id="8a819-126">Durdurulacak kaynak grubu dağıtımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a819-126">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a819-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="8a819-127">-Name</span></span>
<span data-ttu-id="8a819-128">Durdurulacak kaynak grubu dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a819-128">Specifies the name of the resource group deployment to stop.</span></span>

<span data-ttu-id="8a819-129">Bu parametreyi belirtmezseniz, bu cmdlet kaynak grubunda çalışan bir dağıtımı arar ve bunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="8a819-129">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="8a819-130">Birden fazla çalışan dağıtım bulursa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="8a819-130">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="8a819-131">Dağıtım adını almak için Get-AzureRmResourceGroupDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8a819-131">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a819-132">-Pre-</span><span class="sxs-lookup"><span data-stu-id="8a819-132">-Pre</span></span>
<span data-ttu-id="8a819-133">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a819-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a819-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a819-134">-ResourceGroupName</span></span>
<span data-ttu-id="8a819-135">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a819-135">Specifies the name of the resource group.</span></span>
<span data-ttu-id="8a819-136">Bu cmdlet, bu parametrenin belirttiği kaynak grubunun dağıtımını durdurur.</span><span class="sxs-lookup"><span data-stu-id="8a819-136">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a819-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="8a819-137">-Confirm</span></span>
<span data-ttu-id="8a819-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8a819-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a819-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a819-139">-WhatIf</span></span>
<span data-ttu-id="8a819-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a819-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a819-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8a819-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a819-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a819-142">CommonParameters</span></span>
<span data-ttu-id="8a819-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a819-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a819-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a819-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a819-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a819-145">INPUTS</span></span>

### <span data-ttu-id="8a819-146">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8a819-146">None</span></span>

## <span data-ttu-id="8a819-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a819-147">OUTPUTS</span></span>

### <span data-ttu-id="8a819-148">Boole</span><span class="sxs-lookup"><span data-stu-id="8a819-148">Boolean</span></span>

## <span data-ttu-id="8a819-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a819-149">NOTES</span></span>

## <span data-ttu-id="8a819-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a819-150">RELATED LINKS</span></span>

[<span data-ttu-id="8a819-151">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8a819-151">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8a819-152">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8a819-152">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="8a819-153">Yeni-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8a819-153">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="8a819-154">Yeni-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8a819-154">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8a819-155">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8a819-155">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8a819-156">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8a819-156">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


