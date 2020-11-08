---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 1db46630ea4f864e1658eea8b789a79e6050fbbb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108055"
---
# <span data-ttu-id="6f724-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f724-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="6f724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f724-102">SYNOPSIS</span></span>
<span data-ttu-id="6f724-103">Kaynak grubundaki dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="6f724-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="6f724-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f724-104">SYNTAX</span></span>

### <span data-ttu-id="6f724-105">GetByResourceGroupDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6f724-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f724-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="6f724-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f724-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f724-107">DESCRIPTION</span></span>
<span data-ttu-id="6f724-108">**Get-AzResourceGroupDeployment** cmdlet 'ı bir Azure Kaynak grubunda dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="6f724-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="6f724-109">Sonuçları filtrelemek için *ad* veya *ID* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="6f724-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="6f724-110">Varsayılan olarak **Get-AzResourceGroupDeployment** belirtilen bir kaynak grubunun tüm dağıtımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6f724-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="6f724-111">Azure kaynağı, veritabanı sunucusu, veritabanı veya Web sitesi gibi kullanıcı tarafından yönetilen bir Azure varlıksitesidir.</span><span class="sxs-lookup"><span data-stu-id="6f724-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="6f724-112">Bir Azure Kaynak grubu, birim olarak dağıtılan bir Azure kaynakları koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="6f724-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="6f724-113">Dağıtım, kaynak grubundaki kaynakların kullanılabilmesini sağlayan bir işlemdir.</span><span class="sxs-lookup"><span data-stu-id="6f724-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="6f724-114">Azure kaynakları ve Azure Resource Groups hakkında daha fazla bilgi için New-AzResourceGroup cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="6f724-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="6f724-115">Bu cmdlet 'i izleme için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6f724-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="6f724-116">Hata ayıklama için, bu cmdlet 'i Get-AzLog cmdlet ile kullanın.</span><span class="sxs-lookup"><span data-stu-id="6f724-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="6f724-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f724-117">EXAMPLES</span></span>

### <span data-ttu-id="6f724-118">Örnek 1: kaynak grubu için tüm dağıtımları alma</span><span class="sxs-lookup"><span data-stu-id="6f724-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="6f724-119">Bu komut, ContosoLabsRG kaynak grubu için tüm dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="6f724-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="6f724-120">Çıktıda, Galeri şablonu kullanan bir WordPress blogu için dağıtım gösterilir.</span><span class="sxs-lookup"><span data-stu-id="6f724-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="6f724-121">Örnek 2: ada göre dağıtım alma</span><span class="sxs-lookup"><span data-stu-id="6f724-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="6f724-122">Bu komut, ContosoLabsRG kaynak grubunun DeployWebsite01 dağıtımını alır.</span><span class="sxs-lookup"><span data-stu-id="6f724-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="6f724-123">**Yeni-AzResourceGroup** veya **New-AzResourceGroupDeployment** cmdlet 'lerini kullanarak bir dağıtıma bir ad atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6f724-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="6f724-124">Bir ad atamazsanız, cmdlet 'ler dağıtımı oluşturmak için kullanılan şablona dayalı olarak varsayılan bir ad sağlar.</span><span class="sxs-lookup"><span data-stu-id="6f724-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="6f724-125">Örnek 3: tüm kaynak gruplarının dağıtımlarını alma</span><span class="sxs-lookup"><span data-stu-id="6f724-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="6f724-126">Bu komut, Get-AzResourceGroup cmdlet 'ini kullanarak aboneliğinizdeki tüm kaynak gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="6f724-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="6f724-127">Komut, ardışık düzen işlecini kullanarak kaynak gruplarını geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="6f724-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6f724-128">Geçerli cmdlet, abonelikteki tüm kaynak gruplarının tüm dağıtımlarını alır ve onları **Resourcegroupname** , **DeploymentName** ve **provisioningstate** özellik değerlerini görüntülemek için Format-Table cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="6f724-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="6f724-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f724-129">PARAMETERS</span></span>

### <span data-ttu-id="6f724-130">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="6f724-130">-ApiVersion</span></span>
<span data-ttu-id="6f724-131">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f724-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="6f724-132">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6f724-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="6f724-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f724-133">-DefaultProfile</span></span>
<span data-ttu-id="6f724-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6f724-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f724-135">-ID</span><span class="sxs-lookup"><span data-stu-id="6f724-135">-Id</span></span>
<span data-ttu-id="6f724-136">Alınacak kaynak grubu dağıtımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f724-136">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f724-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="6f724-137">-Name</span></span>
<span data-ttu-id="6f724-138">Alınacak dağıtımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f724-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="6f724-139">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="6f724-139">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f724-140">-Pre-</span><span class="sxs-lookup"><span data-stu-id="6f724-140">-Pre</span></span>
<span data-ttu-id="6f724-141">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f724-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6f724-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f724-142">-ResourceGroupName</span></span>
<span data-ttu-id="6f724-143">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f724-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="6f724-144">Cmdlet, bu parametrenin belirttiği kaynak grubunun dağıtımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6f724-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="6f724-145">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="6f724-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="6f724-146">Bu parametre gereklidir ve her komutta yalnızca bir kaynak grubu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6f724-146">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f724-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f724-147">CommonParameters</span></span>
<span data-ttu-id="6f724-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f724-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f724-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6f724-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f724-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f724-150">INPUTS</span></span>

### <span data-ttu-id="6f724-151">System. String</span><span class="sxs-lookup"><span data-stu-id="6f724-151">System.String</span></span>

## <span data-ttu-id="6f724-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f724-152">OUTPUTS</span></span>

### <span data-ttu-id="6f724-153">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f724-153">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="6f724-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f724-154">NOTES</span></span>

## <span data-ttu-id="6f724-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f724-155">RELATED LINKS</span></span>

[<span data-ttu-id="6f724-156">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6f724-156">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="6f724-157">Yeni-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6f724-157">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="6f724-158">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f724-158">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="6f724-159">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f724-159">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="6f724-160">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f724-160">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="6f724-161">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f724-161">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


