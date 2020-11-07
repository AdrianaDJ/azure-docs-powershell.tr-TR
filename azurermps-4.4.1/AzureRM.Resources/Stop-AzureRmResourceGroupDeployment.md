---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: f07b2f59f1a38aca780e1e869bb3904725df6dcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764777"
---
# <span data-ttu-id="b0141-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b0141-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="b0141-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0141-102">SYNOPSIS</span></span>
<span data-ttu-id="b0141-103">Kaynak grubu dağıtımını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="b0141-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0141-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b0141-104">SYNTAX</span></span>

### <span data-ttu-id="b0141-105">Dağıtım adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="b0141-105">The deployment name parameter set.</span></span> <span data-ttu-id="b0141-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="b0141-106">(Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0141-107">Dağıtım kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="b0141-107">The deployment Id parameter set.</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0141-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b0141-108">DESCRIPTION</span></span>
<span data-ttu-id="b0141-109">**Stop-AzureRmResourceGroupDeployment** cmdlet 'i, başlatılmış ancak tamamlanmamış bir Azure Kaynak grubu dağıtımını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="b0141-109">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="b0141-110">Bir dağıtımı durdurmak için dağıtımın, sağlama gibi tamamlanmamış bir sağlama durumu olmalıdır; bunun sağlanması veya başarısız gibi tamamlanmamış bir durumda olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b0141-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="b0141-111">Azure kaynağı, Web sitesi, veritabanı veya veritabanı sunucusu gibi kullanıcı tarafından yönetilen bir varlıktır.</span><span class="sxs-lookup"><span data-stu-id="b0141-111">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="b0141-112">Kaynak grubu, birim olarak dağıtılan kaynaklar topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="b0141-112">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="b0141-113">Kaynak grubu dağıtmak için New-AzureRmResourceGroupDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b0141-113">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>

<span data-ttu-id="b0141-114">New-AzureRmResource cmdlet 'i yeni bir kaynak oluşturur, ancak bu cmdlet 'in durdurmadığı bir kaynak grubu dağıtım işlemini tetiklemez.</span><span class="sxs-lookup"><span data-stu-id="b0141-114">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="b0141-115">Bu cmdlet yalnızca bir çalışan dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="b0141-115">This cmdlet stops only one running deployment.</span></span>

<span data-ttu-id="b0141-116">Belirli bir dağıtımı durdurmak için *Name* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b0141-116">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="b0141-117">*Name* parametresini atlarsanız, **stop-AzureRmResourceGroupDeployment** çalışan bir dağıtımı arar ve bunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="b0141-117">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="b0141-118">Cmdlet birden fazla çalışan dağıtım bulursa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="b0141-118">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="b0141-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b0141-119">EXAMPLES</span></span>

## <span data-ttu-id="b0141-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b0141-120">PARAMETERS</span></span>

### <span data-ttu-id="b0141-121">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="b0141-121">-ApiVersion</span></span>
<span data-ttu-id="b0141-122">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0141-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b0141-123">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0141-123">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0141-124">-ID</span><span class="sxs-lookup"><span data-stu-id="b0141-124">-Id</span></span>
<span data-ttu-id="b0141-125">Durdurulacak kaynak grubu dağıtımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0141-125">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0141-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="b0141-126">-Name</span></span>
<span data-ttu-id="b0141-127">Durdurulacak kaynak grubu dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0141-127">Specifies the name of the resource group deployment to stop.</span></span>

<span data-ttu-id="b0141-128">Bu parametreyi belirtmezseniz, bu cmdlet kaynak grubunda çalışan bir dağıtımı arar ve bunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="b0141-128">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="b0141-129">Birden fazla çalışan dağıtım bulursa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="b0141-129">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="b0141-130">Dağıtım adını almak için Get-AzureRmResourceGroupDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b0141-130">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0141-131">-Pre-</span><span class="sxs-lookup"><span data-stu-id="b0141-131">-Pre</span></span>
<span data-ttu-id="b0141-132">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b0141-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b0141-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0141-133">-ResourceGroupName</span></span>
<span data-ttu-id="b0141-134">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0141-134">Specifies the name of the resource group.</span></span>
<span data-ttu-id="b0141-135">Bu cmdlet, bu parametrenin belirttiği kaynak grubunun dağıtımını durdurur.</span><span class="sxs-lookup"><span data-stu-id="b0141-135">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0141-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="b0141-136">-Confirm</span></span>
<span data-ttu-id="b0141-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b0141-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0141-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0141-138">-WhatIf</span></span>
<span data-ttu-id="b0141-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b0141-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0141-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b0141-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0141-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0141-141">-DefaultProfile</span></span>
<span data-ttu-id="b0141-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b0141-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0141-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0141-143">CommonParameters</span></span>
<span data-ttu-id="b0141-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b0141-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0141-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0141-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0141-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b0141-146">INPUTS</span></span>

### <span data-ttu-id="b0141-147">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b0141-147">None</span></span>

## <span data-ttu-id="b0141-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b0141-148">OUTPUTS</span></span>

### <span data-ttu-id="b0141-149">Boole</span><span class="sxs-lookup"><span data-stu-id="b0141-149">Boolean</span></span>

## <span data-ttu-id="b0141-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b0141-150">NOTES</span></span>

## <span data-ttu-id="b0141-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b0141-151">RELATED LINKS</span></span>

[<span data-ttu-id="b0141-152">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b0141-152">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b0141-153">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b0141-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="b0141-154">Yeni-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b0141-154">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="b0141-155">Yeni-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b0141-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b0141-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b0141-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b0141-157">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b0141-157">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


