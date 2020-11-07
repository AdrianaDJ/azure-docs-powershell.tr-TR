---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 139b38fed6e768e761631687f06cd833afaa4068
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938755"
---
# <span data-ttu-id="bdb30-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bdb30-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="bdb30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdb30-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb30-103">Kaynak grubu dağıtımını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="bdb30-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdb30-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bdb30-104">SYNTAX</span></span>

### <span data-ttu-id="bdb30-105">StopByResourceGroupDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bdb30-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdb30-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="bdb30-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdb30-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bdb30-107">DESCRIPTION</span></span>
<span data-ttu-id="bdb30-108">**Stop-AzureRmResourceGroupDeployment** cmdlet 'i, başlatılmış ancak tamamlanmamış bir Azure Kaynak grubu dağıtımını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="bdb30-108">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="bdb30-109">Bir dağıtımı durdurmak için dağıtımın, sağlama gibi tamamlanmamış bir sağlama durumu olmalıdır; bunun sağlanması veya başarısız gibi tamamlanmamış bir durumda olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="bdb30-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="bdb30-110">Azure kaynağı, Web sitesi, veritabanı veya veritabanı sunucusu gibi kullanıcı tarafından yönetilen bir varlıktır.</span><span class="sxs-lookup"><span data-stu-id="bdb30-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="bdb30-111">Kaynak grubu, birim olarak dağıtılan kaynaklar topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="bdb30-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="bdb30-112">Kaynak grubu dağıtmak için New-AzureRmResourceGroupDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bdb30-112">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="bdb30-113">New-AzureRmResource cmdlet 'i yeni bir kaynak oluşturur, ancak bu cmdlet 'in durdurmadığı bir kaynak grubu dağıtım işlemini tetiklemez.</span><span class="sxs-lookup"><span data-stu-id="bdb30-113">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="bdb30-114">Bu cmdlet yalnızca bir çalışan dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="bdb30-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="bdb30-115">Belirli bir dağıtımı durdurmak için *Name* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bdb30-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="bdb30-116">*Name* parametresini atlarsanız, **stop-AzureRmResourceGroupDeployment** çalışan bir dağıtımı arar ve bunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="bdb30-116">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="bdb30-117">Cmdlet birden fazla çalışan dağıtım bulursa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="bdb30-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="bdb30-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bdb30-118">EXAMPLES</span></span>

### <span data-ttu-id="bdb30-119">Örnek 1: kaynak grubu dağıtımını başlatma ve durdurma</span><span class="sxs-lookup"><span data-stu-id="bdb30-119">Example 1: Starting and stopping a resource group deployment</span></span>

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

## <span data-ttu-id="bdb30-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bdb30-120">PARAMETERS</span></span>

### <span data-ttu-id="bdb30-121">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="bdb30-121">-ApiVersion</span></span>
<span data-ttu-id="bdb30-122">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdb30-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="bdb30-123">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bdb30-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="bdb30-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb30-124">-DefaultProfile</span></span>
<span data-ttu-id="bdb30-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bdb30-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdb30-126">-ID</span><span class="sxs-lookup"><span data-stu-id="bdb30-126">-Id</span></span>
<span data-ttu-id="bdb30-127">Durdurulacak kaynak grubu dağıtımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdb30-127">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="bdb30-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="bdb30-128">-Name</span></span>
<span data-ttu-id="bdb30-129">Durdurulacak kaynak grubu dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdb30-129">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="bdb30-130">Bu parametreyi belirtmezseniz, bu cmdlet kaynak grubunda çalışan bir dağıtımı arar ve bunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="bdb30-130">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="bdb30-131">Birden fazla çalışan dağıtım bulursa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="bdb30-131">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="bdb30-132">Dağıtım adını almak için Get-AzureRmResourceGroupDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bdb30-132">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

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

### <span data-ttu-id="bdb30-133">-Pre-</span><span class="sxs-lookup"><span data-stu-id="bdb30-133">-Pre</span></span>
<span data-ttu-id="bdb30-134">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bdb30-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bdb30-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdb30-135">-ResourceGroupName</span></span>
<span data-ttu-id="bdb30-136">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdb30-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="bdb30-137">Bu cmdlet, bu parametrenin belirttiği kaynak grubunun dağıtımını durdurur.</span><span class="sxs-lookup"><span data-stu-id="bdb30-137">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bdb30-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="bdb30-138">-Confirm</span></span>
<span data-ttu-id="bdb30-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bdb30-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdb30-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdb30-140">-WhatIf</span></span>
<span data-ttu-id="bdb30-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bdb30-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdb30-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bdb30-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdb30-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb30-143">CommonParameters</span></span>
<span data-ttu-id="bdb30-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bdb30-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb30-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdb30-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb30-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bdb30-146">INPUTS</span></span>

### <span data-ttu-id="bdb30-147">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bdb30-147">None</span></span>

## <span data-ttu-id="bdb30-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bdb30-148">OUTPUTS</span></span>

### <span data-ttu-id="bdb30-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bdb30-149">System.Boolean</span></span>

## <span data-ttu-id="bdb30-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bdb30-150">NOTES</span></span>

## <span data-ttu-id="bdb30-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bdb30-151">RELATED LINKS</span></span>

[<span data-ttu-id="bdb30-152">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bdb30-152">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="bdb30-153">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="bdb30-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="bdb30-154">Yeni-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bdb30-154">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="bdb30-155">Yeni-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bdb30-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="bdb30-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bdb30-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="bdb30-157">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bdb30-157">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


