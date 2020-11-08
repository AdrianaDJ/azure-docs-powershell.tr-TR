---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: fa189637c9c2c1b63ab0e8dd0b00fab3f4505da0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275691"
---
# <span data-ttu-id="94a78-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="94a78-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="94a78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94a78-102">SYNOPSIS</span></span>
<span data-ttu-id="94a78-103">Kaynak grubu dağıtımını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="94a78-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="94a78-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94a78-104">SYNTAX</span></span>

### <span data-ttu-id="94a78-105">StopByResourceGroupDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="94a78-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94a78-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="94a78-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94a78-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="94a78-107">DESCRIPTION</span></span>
<span data-ttu-id="94a78-108">**Stop-AzResourceGroupDeployment** cmdlet 'i, başlatılmış ancak tamamlanmamış bir Azure Kaynak grubu dağıtımını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="94a78-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="94a78-109">Bir dağıtımı durdurmak için dağıtımın, sağlama gibi tamamlanmamış bir sağlama durumu olmalıdır; bunun sağlanması veya başarısız gibi tamamlanmamış bir durumda olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="94a78-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="94a78-110">Azure kaynağı, Web sitesi, veritabanı veya veritabanı sunucusu gibi kullanıcı tarafından yönetilen bir varlıktır.</span><span class="sxs-lookup"><span data-stu-id="94a78-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="94a78-111">Kaynak grubu, birim olarak dağıtılan kaynaklar topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="94a78-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="94a78-112">Kaynak grubu dağıtmak için New-AzResourceGroupDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="94a78-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="94a78-113">New-AzResource cmdlet 'i yeni bir kaynak oluşturur, ancak bu cmdlet 'in durdurmadığı bir kaynak grubu dağıtım işlemini tetiklemez.</span><span class="sxs-lookup"><span data-stu-id="94a78-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="94a78-114">Bu cmdlet yalnızca bir çalışan dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="94a78-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="94a78-115">Belirli bir dağıtımı durdurmak için *Name* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="94a78-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="94a78-116">*Name* parametresini atlarsanız, **stop-AzResourceGroupDeployment** çalışan bir dağıtımı arar ve bunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="94a78-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="94a78-117">Cmdlet birden fazla çalışan dağıtım bulursa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="94a78-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="94a78-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94a78-118">EXAMPLES</span></span>

### <span data-ttu-id="94a78-119">Örnek 1: kaynak grubu dağıtımını başlatma ve durdurma</span><span class="sxs-lookup"><span data-stu-id="94a78-119">Example 1: Starting and stopping a resource group deployment</span></span>

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

## <span data-ttu-id="94a78-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94a78-120">PARAMETERS</span></span>

### <span data-ttu-id="94a78-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a78-121">-DefaultProfile</span></span>
<span data-ttu-id="94a78-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="94a78-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94a78-123">-ID</span><span class="sxs-lookup"><span data-stu-id="94a78-123">-Id</span></span>
<span data-ttu-id="94a78-124">Durdurulacak kaynak grubu dağıtımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="94a78-124">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="94a78-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="94a78-125">-Name</span></span>
<span data-ttu-id="94a78-126">Durdurulacak kaynak grubu dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94a78-126">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="94a78-127">Bu parametreyi belirtmezseniz, bu cmdlet kaynak grubunda çalışan bir dağıtımı arar ve bunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="94a78-127">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="94a78-128">Birden fazla çalışan dağıtım bulursa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="94a78-128">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="94a78-129">Dağıtım adını almak için Get-AzResourceGroupDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="94a78-129">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

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

### <span data-ttu-id="94a78-130">-Pre-</span><span class="sxs-lookup"><span data-stu-id="94a78-130">-Pre</span></span>
<span data-ttu-id="94a78-131">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="94a78-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="94a78-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94a78-132">-ResourceGroupName</span></span>
<span data-ttu-id="94a78-133">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94a78-133">Specifies the name of the resource group.</span></span>
<span data-ttu-id="94a78-134">Bu cmdlet, bu parametrenin belirttiği kaynak grubunun dağıtımını durdurur.</span><span class="sxs-lookup"><span data-stu-id="94a78-134">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="94a78-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="94a78-135">-Confirm</span></span>
<span data-ttu-id="94a78-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="94a78-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94a78-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94a78-137">-WhatIf</span></span>
<span data-ttu-id="94a78-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="94a78-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94a78-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="94a78-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94a78-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a78-140">CommonParameters</span></span>
<span data-ttu-id="94a78-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94a78-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a78-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="94a78-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a78-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94a78-143">INPUTS</span></span>

### <span data-ttu-id="94a78-144">System. String</span><span class="sxs-lookup"><span data-stu-id="94a78-144">System.String</span></span>

## <span data-ttu-id="94a78-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94a78-145">OUTPUTS</span></span>

### <span data-ttu-id="94a78-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="94a78-146">System.Boolean</span></span>

## <span data-ttu-id="94a78-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94a78-147">NOTES</span></span>

## <span data-ttu-id="94a78-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94a78-148">RELATED LINKS</span></span>

[<span data-ttu-id="94a78-149">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="94a78-149">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="94a78-150">Yeni-aza kaynağı</span><span class="sxs-lookup"><span data-stu-id="94a78-150">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="94a78-151">Yeni-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94a78-151">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="94a78-152">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="94a78-152">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="94a78-153">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="94a78-153">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="94a78-154">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="94a78-154">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


