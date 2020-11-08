---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: 2daec87c79e02d6aa4d2720bb20cac5194d1a752
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933292"
---
# <span data-ttu-id="7c6f2-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7c6f2-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="7c6f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c6f2-102">SYNOPSIS</span></span>
<span data-ttu-id="7c6f2-103">Kaynak grubu dağıtımını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="7c6f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7c6f2-104">SYNTAX</span></span>

### <span data-ttu-id="7c6f2-105">StopByResourceGroupDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7c6f2-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c6f2-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="7c6f2-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c6f2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c6f2-107">DESCRIPTION</span></span>
<span data-ttu-id="7c6f2-108">**Stop-AzResourceGroupDeployment** cmdlet 'i, başlatılmış ancak tamamlanmamış bir Azure Kaynak grubu dağıtımını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="7c6f2-109">Bir dağıtımı durdurmak için dağıtımın, sağlama gibi tamamlanmamış bir sağlama durumu olmalıdır; bunun sağlanması veya başarısız gibi tamamlanmamış bir durumda olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="7c6f2-110">Azure kaynağı, Web sitesi, veritabanı veya veritabanı sunucusu gibi kullanıcı tarafından yönetilen bir varlıktır.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="7c6f2-111">Kaynak grubu, birim olarak dağıtılan kaynaklar topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="7c6f2-112">Kaynak grubu dağıtmak için New-AzResourceGroupDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="7c6f2-113">New-AzResource cmdlet 'i yeni bir kaynak oluşturur, ancak bu cmdlet 'in durdurmadığı bir kaynak grubu dağıtım işlemini tetiklemez.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="7c6f2-114">Bu cmdlet yalnızca bir çalışan dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="7c6f2-115">Belirli bir dağıtımı durdurmak için *Name* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="7c6f2-116">*Name* parametresini atlarsanız, **stop-AzResourceGroupDeployment** çalışan bir dağıtımı arar ve bunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="7c6f2-117">Cmdlet birden fazla çalışan dağıtım bulursa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="7c6f2-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7c6f2-118">EXAMPLES</span></span>

### <span data-ttu-id="7c6f2-119">Örnek 1: kaynak grubu dağıtımını başlatma ve durdurma</span><span class="sxs-lookup"><span data-stu-id="7c6f2-119">Example 1: Starting and stopping a resource group deployment</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg -TemplateFile .\storage-account-create-azdeploy.json -TemplateParameterFile .\storage-account-create-azdeploy.parameters.json -AsJob

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            New-AzResourceGro...

PS C:\> Stop-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg
True

PS C:\> Get-Job 1

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Failed        True            localhost            New-AzResourceGro...
```

## <span data-ttu-id="7c6f2-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7c6f2-120">PARAMETERS</span></span>

### <span data-ttu-id="7c6f2-121">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="7c6f2-121">-ApiVersion</span></span>
<span data-ttu-id="7c6f2-122">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="7c6f2-123">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="7c6f2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c6f2-124">-DefaultProfile</span></span>
<span data-ttu-id="7c6f2-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7c6f2-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c6f2-126">-ID</span><span class="sxs-lookup"><span data-stu-id="7c6f2-126">-Id</span></span>
<span data-ttu-id="7c6f2-127">Durdurulacak kaynak grubu dağıtımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-127">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="7c6f2-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="7c6f2-128">-Name</span></span>
<span data-ttu-id="7c6f2-129">Durdurulacak kaynak grubu dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-129">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="7c6f2-130">Bu parametreyi belirtmezseniz, bu cmdlet kaynak grubunda çalışan bir dağıtımı arar ve bunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-130">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="7c6f2-131">Birden fazla çalışan dağıtım bulursa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-131">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="7c6f2-132">Dağıtım adını almak için Get-AzResourceGroupDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-132">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

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

### <span data-ttu-id="7c6f2-133">-Pre-</span><span class="sxs-lookup"><span data-stu-id="7c6f2-133">-Pre</span></span>
<span data-ttu-id="7c6f2-134">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7c6f2-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c6f2-135">-ResourceGroupName</span></span>
<span data-ttu-id="7c6f2-136">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="7c6f2-137">Bu cmdlet, bu parametrenin belirttiği kaynak grubunun dağıtımını durdurur.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-137">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7c6f2-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="7c6f2-138">-Confirm</span></span>
<span data-ttu-id="7c6f2-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c6f2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c6f2-140">-WhatIf</span></span>
<span data-ttu-id="7c6f2-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c6f2-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c6f2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c6f2-143">CommonParameters</span></span>
<span data-ttu-id="7c6f2-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c6f2-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c6f2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c6f2-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7c6f2-146">INPUTS</span></span>

### <span data-ttu-id="7c6f2-147">System. String</span><span class="sxs-lookup"><span data-stu-id="7c6f2-147">System.String</span></span>

## <span data-ttu-id="7c6f2-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7c6f2-148">OUTPUTS</span></span>

### <span data-ttu-id="7c6f2-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7c6f2-149">System.Boolean</span></span>

## <span data-ttu-id="7c6f2-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7c6f2-150">NOTES</span></span>

## <span data-ttu-id="7c6f2-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7c6f2-151">RELATED LINKS</span></span>

[<span data-ttu-id="7c6f2-152">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7c6f2-152">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="7c6f2-153">Yeni-aza kaynağı</span><span class="sxs-lookup"><span data-stu-id="7c6f2-153">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="7c6f2-154">Yeni-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7c6f2-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="7c6f2-155">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7c6f2-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="7c6f2-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7c6f2-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="7c6f2-157">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7c6f2-157">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)

