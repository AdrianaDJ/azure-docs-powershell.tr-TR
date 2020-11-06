---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: c9a144e92c4950d927177d4cbcb921c245c18b98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593894"
---
# <span data-ttu-id="191df-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191df-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="191df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="191df-102">SYNOPSIS</span></span>
<span data-ttu-id="191df-103">Kaynak grubu dağıtımını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="191df-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="191df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="191df-104">SYNTAX</span></span>

### <span data-ttu-id="191df-105">StopByResourceGroupDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="191df-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="191df-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="191df-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="191df-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="191df-107">DESCRIPTION</span></span>
<span data-ttu-id="191df-108">**Stop-AzureRmResourceGroupDeployment** cmdlet 'i, başlatılmış ancak tamamlanmamış bir Azure Kaynak grubu dağıtımını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="191df-108">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="191df-109">Bir dağıtımı durdurmak için dağıtımın, sağlama gibi tamamlanmamış bir sağlama durumu olmalıdır; bunun sağlanması veya başarısız gibi tamamlanmamış bir durumda olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="191df-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="191df-110">Azure kaynağı, Web sitesi, veritabanı veya veritabanı sunucusu gibi kullanıcı tarafından yönetilen bir varlıktır.</span><span class="sxs-lookup"><span data-stu-id="191df-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="191df-111">Kaynak grubu, birim olarak dağıtılan kaynaklar topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="191df-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="191df-112">Kaynak grubu dağıtmak için New-AzureRmResourceGroupDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="191df-112">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="191df-113">New-AzureRmResource cmdlet 'i yeni bir kaynak oluşturur, ancak bu cmdlet 'in durdurmadığı bir kaynak grubu dağıtım işlemini tetiklemez.</span><span class="sxs-lookup"><span data-stu-id="191df-113">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="191df-114">Bu cmdlet yalnızca bir çalışan dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="191df-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="191df-115">Belirli bir dağıtımı durdurmak için *Name* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="191df-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="191df-116">*Name* parametresini atlarsanız, **stop-AzureRmResourceGroupDeployment** çalışan bir dağıtımı arar ve bunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="191df-116">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="191df-117">Cmdlet birden fazla çalışan dağıtım bulursa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="191df-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="191df-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="191df-118">EXAMPLES</span></span>

### <span data-ttu-id="191df-119">Örnek 1: kaynak grubu dağıtımını başlatma ve durdurma</span><span class="sxs-lookup"><span data-stu-id="191df-119">Example 1: Starting and stopping a resource group deployment</span></span>

```powershell
PS C:\> New-AzureRmResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg -TemplateFile .\storage-account-create-azuredeploy.json -TemplateParameterFile .\storage-account-create-azuredeploy.parameters.json -AsJob

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmResourceGro...

PS C:\> Stop-AzureRmResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg
True

PS C:\> Get-Job 1

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Failed        True            localhost            New-AzureRmResourceGro...
```

## <span data-ttu-id="191df-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="191df-120">PARAMETERS</span></span>

### <span data-ttu-id="191df-121">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="191df-121">-ApiVersion</span></span>
<span data-ttu-id="191df-122">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="191df-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="191df-123">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="191df-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="191df-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="191df-124">-DefaultProfile</span></span>
<span data-ttu-id="191df-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="191df-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="191df-126">-ID</span><span class="sxs-lookup"><span data-stu-id="191df-126">-Id</span></span>
<span data-ttu-id="191df-127">Durdurulacak kaynak grubu dağıtımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="191df-127">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="191df-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="191df-128">-Name</span></span>
<span data-ttu-id="191df-129">Durdurulacak kaynak grubu dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="191df-129">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="191df-130">Bu parametreyi belirtmezseniz, bu cmdlet kaynak grubunda çalışan bir dağıtımı arar ve bunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="191df-130">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="191df-131">Birden fazla çalışan dağıtım bulursa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="191df-131">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="191df-132">Dağıtım adını almak için Get-AzureRmResourceGroupDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="191df-132">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="191df-133">-Pre-</span><span class="sxs-lookup"><span data-stu-id="191df-133">-Pre</span></span>
<span data-ttu-id="191df-134">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="191df-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="191df-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="191df-135">-ResourceGroupName</span></span>
<span data-ttu-id="191df-136">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="191df-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="191df-137">Bu cmdlet, bu parametrenin belirttiği kaynak grubunun dağıtımını durdurur.</span><span class="sxs-lookup"><span data-stu-id="191df-137">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="191df-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="191df-138">-Confirm</span></span>
<span data-ttu-id="191df-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="191df-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="191df-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="191df-140">-WhatIf</span></span>
<span data-ttu-id="191df-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="191df-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="191df-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="191df-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="191df-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="191df-143">CommonParameters</span></span>
<span data-ttu-id="191df-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="191df-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="191df-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="191df-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="191df-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="191df-146">INPUTS</span></span>

### <span data-ttu-id="191df-147">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="191df-147">None</span></span>

## <span data-ttu-id="191df-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="191df-148">OUTPUTS</span></span>

### <span data-ttu-id="191df-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="191df-149">System.Boolean</span></span>

## <span data-ttu-id="191df-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="191df-150">NOTES</span></span>

## <span data-ttu-id="191df-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="191df-151">RELATED LINKS</span></span>

[<span data-ttu-id="191df-152">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191df-152">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="191df-153">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="191df-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="191df-154">Yeni-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="191df-154">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="191df-155">Yeni-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191df-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="191df-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191df-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="191df-157">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191df-157">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


