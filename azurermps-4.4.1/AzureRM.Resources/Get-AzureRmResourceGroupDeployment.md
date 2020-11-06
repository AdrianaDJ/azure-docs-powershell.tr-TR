---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: e64fdd0300f2ccad4c3904d472563bbc30374b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592578"
---
# <span data-ttu-id="7040c-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7040c-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="7040c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7040c-102">SYNOPSIS</span></span>
<span data-ttu-id="7040c-103">Kaynak grubundaki dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="7040c-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7040c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7040c-104">SYNTAX</span></span>

### <span data-ttu-id="7040c-105">Dağıtım adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="7040c-105">The deployment name parameter set.</span></span> <span data-ttu-id="7040c-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="7040c-106">(Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7040c-107">Dağıtım kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="7040c-107">The deployment Id parameter set.</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7040c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7040c-108">DESCRIPTION</span></span>
<span data-ttu-id="7040c-109">**Get-AzureRmResourceGroupDeployment** cmdlet 'ı bir Azure Kaynak grubunda dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="7040c-109">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="7040c-110">Sonuçları filtrelemek için *ad* veya *ID* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="7040c-110">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="7040c-111">Varsayılan olarak **Get-AzureRmResourceGroupDeployment** belirtilen bir kaynak grubu için tüm dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="7040c-111">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>

<span data-ttu-id="7040c-112">Azure kaynağı, veritabanı sunucusu, veritabanı veya Web sitesi gibi kullanıcı tarafından yönetilen bir Azure varlıksitesidir.</span><span class="sxs-lookup"><span data-stu-id="7040c-112">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="7040c-113">Bir Azure Kaynak grubu, birim olarak dağıtılan bir Azure kaynakları koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="7040c-113">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

<span data-ttu-id="7040c-114">Dağıtım, kaynak grubundaki kaynakların kullanılabilmesini sağlayan bir işlemdir.</span><span class="sxs-lookup"><span data-stu-id="7040c-114">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="7040c-115">Azure kaynakları ve Azure Resource Groups hakkında daha fazla bilgi için New-AzureRmResourceGroup cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="7040c-115">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="7040c-116">Bu cmdlet 'i izleme için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7040c-116">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="7040c-117">Hata ayıklama için, bu cmdlet 'i Get-AzureRmLog cmdlet ile kullanın.</span><span class="sxs-lookup"><span data-stu-id="7040c-117">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="7040c-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7040c-118">EXAMPLES</span></span>

### <span data-ttu-id="7040c-119">Örnek 1: kaynak grubu için tüm dağıtımları alma</span><span class="sxs-lookup"><span data-stu-id="7040c-119">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="7040c-120">Bu komut, ContosoLabsRG kaynak grubu için tüm dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="7040c-120">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="7040c-121">Çıktıda, Galeri şablonu kullanan bir WordPress blogu için dağıtım gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7040c-121">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="7040c-122">Örnek 2: ada göre dağıtım alma</span><span class="sxs-lookup"><span data-stu-id="7040c-122">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="7040c-123">Bu komut, ContosoLabsRG kaynak grubunun DeployWebsite01 dağıtımını alır.</span><span class="sxs-lookup"><span data-stu-id="7040c-123">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="7040c-124">**Yeni-AzureRmResourceGroup** veya **New-AzureRmResourceGroupDeployment** cmdlet 'lerini kullanarak bir dağıtıma bir ad atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7040c-124">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="7040c-125">Bir ad atamazsanız, cmdlet 'ler dağıtımı oluşturmak için kullanılan şablona dayalı olarak varsayılan bir ad sağlar.</span><span class="sxs-lookup"><span data-stu-id="7040c-125">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="7040c-126">Örnek 3: tüm kaynak gruplarının dağıtımlarını alma</span><span class="sxs-lookup"><span data-stu-id="7040c-126">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="7040c-127">Bu komut, Get-AzureRmResourceGroup cmdlet 'ini kullanarak aboneliğinizdeki tüm kaynak gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="7040c-127">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="7040c-128">Komut, ardışık düzen işlecini kullanarak kaynak gruplarını geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="7040c-128">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7040c-129">Geçerli cmdlet, abonelikteki tüm kaynak gruplarının tüm dağıtımlarını alır ve onları **Resourcegroupname** , **DeploymentName** ve **provisioningstate** özellik değerlerini görüntülemek için Format-Table cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="7040c-129">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="7040c-130">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7040c-130">PARAMETERS</span></span>

### <span data-ttu-id="7040c-131">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="7040c-131">-ApiVersion</span></span>
<span data-ttu-id="7040c-132">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7040c-132">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="7040c-133">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7040c-133">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="7040c-134">-ID</span><span class="sxs-lookup"><span data-stu-id="7040c-134">-Id</span></span>
<span data-ttu-id="7040c-135">Alınacak kaynak grubu dağıtımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7040c-135">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="7040c-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="7040c-136">-Name</span></span>
<span data-ttu-id="7040c-137">Alınacak dağıtımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7040c-137">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="7040c-138">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="7040c-138">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7040c-139">-Pre-</span><span class="sxs-lookup"><span data-stu-id="7040c-139">-Pre</span></span>
<span data-ttu-id="7040c-140">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7040c-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7040c-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7040c-141">-ResourceGroupName</span></span>
<span data-ttu-id="7040c-142">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7040c-142">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7040c-143">Cmdlet, bu parametrenin belirttiği kaynak grubunun dağıtımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="7040c-143">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="7040c-144">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="7040c-144">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="7040c-145">Bu parametre gereklidir ve her komutta yalnızca bir kaynak grubu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7040c-145">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="7040c-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7040c-146">-DefaultProfile</span></span>
<span data-ttu-id="7040c-147">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7040c-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7040c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7040c-148">CommonParameters</span></span>
<span data-ttu-id="7040c-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7040c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7040c-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7040c-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7040c-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7040c-151">INPUTS</span></span>

### <span data-ttu-id="7040c-152">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7040c-152">None</span></span>

## <span data-ttu-id="7040c-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7040c-153">OUTPUTS</span></span>

### <span data-ttu-id="7040c-154">Microsoft. Azure. Commands. ResourceManagement. modeller. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7040c-154">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroupDeployment</span></span>
<span data-ttu-id="7040c-155">Cmdlet kaynak grubu dağıtımlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="7040c-155">The cmdlet returns resource group deployments.</span></span>

## <span data-ttu-id="7040c-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7040c-156">NOTES</span></span>

## <span data-ttu-id="7040c-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7040c-157">RELATED LINKS</span></span>

[<span data-ttu-id="7040c-158">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7040c-158">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="7040c-159">Yeni-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7040c-159">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="7040c-160">Yeni-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7040c-160">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="7040c-161">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7040c-161">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="7040c-162">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7040c-162">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="7040c-163">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7040c-163">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


