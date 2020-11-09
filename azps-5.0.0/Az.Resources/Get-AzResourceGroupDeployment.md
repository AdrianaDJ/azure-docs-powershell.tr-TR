---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 82df573a658fda9af97778e59819e45359c226fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322951"
---
# <span data-ttu-id="3f5f4-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3f5f4-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="3f5f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f5f4-102">SYNOPSIS</span></span>
<span data-ttu-id="3f5f4-103">Kaynak grubundaki dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="3f5f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f5f4-104">SYNTAX</span></span>

### <span data-ttu-id="3f5f4-105">GetByResourceGroupDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3f5f4-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f5f4-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="3f5f4-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f5f4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f5f4-107">DESCRIPTION</span></span>
<span data-ttu-id="3f5f4-108">**Get-AzResourceGroupDeployment** cmdlet 'ı bir Azure Kaynak grubunda dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="3f5f4-109">Sonuçları filtrelemek için *ad* veya *ID* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="3f5f4-110">Varsayılan olarak **Get-AzResourceGroupDeployment** belirtilen bir kaynak grubunun tüm dağıtımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="3f5f4-111">Azure kaynağı, veritabanı sunucusu, veritabanı veya Web sitesi gibi kullanıcı tarafından yönetilen bir Azure varlıksitesidir.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="3f5f4-112">Bir Azure Kaynak grubu, birim olarak dağıtılan bir Azure kaynakları koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="3f5f4-113">Dağıtım, kaynak grubundaki kaynakların kullanılabilmesini sağlayan bir işlemdir.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="3f5f4-114">Azure kaynakları ve Azure Resource Groups hakkında daha fazla bilgi için New-AzResourceGroup cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="3f5f4-115">Bu cmdlet 'i izleme için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="3f5f4-116">Hata ayıklama için, bu cmdlet 'i Get-AzLog cmdlet ile kullanın.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="3f5f4-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f5f4-117">EXAMPLES</span></span>

### <span data-ttu-id="3f5f4-118">Örnek 1: kaynak grubu için tüm dağıtımları alma</span><span class="sxs-lookup"><span data-stu-id="3f5f4-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="3f5f4-119">Bu komut, ContosoLabsRG kaynak grubu için tüm dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="3f5f4-120">Çıktıda, Galeri şablonu kullanan bir WordPress blogu için dağıtım gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="3f5f4-121">Örnek 2: ada göre dağıtım alma</span><span class="sxs-lookup"><span data-stu-id="3f5f4-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="3f5f4-122">Bu komut, ContosoLabsRG kaynak grubunun DeployWebsite01 dağıtımını alır.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="3f5f4-123">**Yeni-AzResourceGroup** veya **New-AzResourceGroupDeployment** cmdlet 'lerini kullanarak bir dağıtıma bir ad atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="3f5f4-124">Bir ad atamazsanız, cmdlet 'ler dağıtımı oluşturmak için kullanılan şablona dayalı olarak varsayılan bir ad sağlar.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="3f5f4-125">Örnek 3: tüm kaynak gruplarının dağıtımlarını alma</span><span class="sxs-lookup"><span data-stu-id="3f5f4-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="3f5f4-126">Bu komut, Get-AzResourceGroup cmdlet 'ini kullanarak aboneliğinizdeki tüm kaynak gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="3f5f4-127">Komut, ardışık düzen işlecini kullanarak kaynak gruplarını geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3f5f4-128">Geçerli cmdlet, abonelikteki tüm kaynak gruplarının tüm dağıtımlarını alır ve onları **Resourcegroupname** , **DeploymentName** ve **provisioningstate** özellik değerlerini görüntülemek için Format-Table cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="3f5f4-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f5f4-129">PARAMETERS</span></span>

### <span data-ttu-id="3f5f4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f5f4-130">-DefaultProfile</span></span>
<span data-ttu-id="3f5f4-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3f5f4-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f5f4-132">-ID</span><span class="sxs-lookup"><span data-stu-id="3f5f4-132">-Id</span></span>
<span data-ttu-id="3f5f4-133">Alınacak kaynak grubu dağıtımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-133">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="3f5f4-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="3f5f4-134">-Name</span></span>
<span data-ttu-id="3f5f4-135">Alınacak dağıtımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-135">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="3f5f4-136">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-136">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="3f5f4-137">-Pre-</span><span class="sxs-lookup"><span data-stu-id="3f5f4-137">-Pre</span></span>
<span data-ttu-id="3f5f4-138">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3f5f4-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f5f4-139">-ResourceGroupName</span></span>
<span data-ttu-id="3f5f4-140">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-140">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3f5f4-141">Cmdlet, bu parametrenin belirttiği kaynak grubunun dağıtımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-141">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="3f5f4-142">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-142">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="3f5f4-143">Bu parametre gereklidir ve her komutta yalnızca bir kaynak grubu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-143">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="3f5f4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f5f4-144">CommonParameters</span></span>
<span data-ttu-id="3f5f4-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f5f4-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3f5f4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f5f4-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f5f4-147">INPUTS</span></span>

### <span data-ttu-id="3f5f4-148">System. String</span><span class="sxs-lookup"><span data-stu-id="3f5f4-148">System.String</span></span>

## <span data-ttu-id="3f5f4-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f5f4-149">OUTPUTS</span></span>

### <span data-ttu-id="3f5f4-150">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3f5f4-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="3f5f4-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f5f4-151">NOTES</span></span>

## <span data-ttu-id="3f5f4-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f5f4-152">RELATED LINKS</span></span>

[<span data-ttu-id="3f5f4-153">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3f5f4-153">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="3f5f4-154">Yeni-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3f5f4-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="3f5f4-155">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3f5f4-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="3f5f4-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3f5f4-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="3f5f4-157">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3f5f4-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="3f5f4-158">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3f5f4-158">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


