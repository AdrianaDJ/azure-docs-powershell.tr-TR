---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: bcc0a4f39b2c5578213aeb3ea5087ce1cc21cc4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751229"
---
# <span data-ttu-id="cd31d-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="cd31d-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="cd31d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd31d-102">SYNOPSIS</span></span>
<span data-ttu-id="cd31d-103">Yönetilen Kubernetes kümesi için Kubectl yapılandırmasını içeri aktarın ve birleştirin.</span><span class="sxs-lookup"><span data-stu-id="cd31d-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="cd31d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd31d-104">SYNTAX</span></span>

### <span data-ttu-id="cd31d-105">GroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cd31d-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd31d-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="cd31d-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd31d-107">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="cd31d-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd31d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd31d-108">DESCRIPTION</span></span>
<span data-ttu-id="cd31d-109">Yönetilen Kubernetes kümesi için Kubectl yapılandırmasını içeri aktarın ve birleştirin.</span><span class="sxs-lookup"><span data-stu-id="cd31d-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="cd31d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd31d-110">EXAMPLES</span></span>

### <span data-ttu-id="cd31d-111">Kubectl yapılandırmasını içeri ve birleştirme</span><span class="sxs-lookup"><span data-stu-id="cd31d-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="cd31d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd31d-112">PARAMETERS</span></span>

### <span data-ttu-id="cd31d-113">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="cd31d-113">-Admin</span></span>
<span data-ttu-id="cd31d-114">Varsayılan ' clusterUser ' yerine ' clusterAdmin' kubectl config 'i alın.</span><span class="sxs-lookup"><span data-stu-id="cd31d-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="cd31d-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="cd31d-115">-ConfigPath</span></span>
<span data-ttu-id="cd31d-116">Oluşturulacak veya güncelleştirilecek bir kubectl yapılandırma dosyası.</span><span class="sxs-lookup"><span data-stu-id="cd31d-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="cd31d-117">Bunun yerine stdout ile</span><span class="sxs-lookup"><span data-stu-id="cd31d-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="cd31d-118">Varsayılan:% giriş%/.Kube/config.</span><span class="sxs-lookup"><span data-stu-id="cd31d-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="cd31d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd31d-119">-DefaultProfile</span></span>
<span data-ttu-id="cd31d-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd31d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd31d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cd31d-121">-Force</span></span>
<span data-ttu-id="cd31d-122">Varsayılan olsa bile Kubernetes yapılandırmasını içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="cd31d-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="cd31d-123">-ID</span><span class="sxs-lookup"><span data-stu-id="cd31d-123">-Id</span></span>
<span data-ttu-id="cd31d-124">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="cd31d-124">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd31d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd31d-125">-InputObject</span></span>
<span data-ttu-id="cd31d-126">Normalde ardışık düzen aracılığıyla iletilen bir PSKubernetesCluster nesnesi.</span><span class="sxs-lookup"><span data-stu-id="cd31d-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd31d-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd31d-127">-Name</span></span>
<span data-ttu-id="cd31d-128">Yönetilen Kubernetes kümeniz adı</span><span class="sxs-lookup"><span data-stu-id="cd31d-128">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd31d-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cd31d-129">-PassThru</span></span>
<span data-ttu-id="cd31d-130">İçeri aktarma işlemi başarılıysa doğru verir</span><span class="sxs-lookup"><span data-stu-id="cd31d-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="cd31d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd31d-131">-ResourceGroupName</span></span>
<span data-ttu-id="cd31d-132">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="cd31d-132">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd31d-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="cd31d-133">-Confirm</span></span>
<span data-ttu-id="cd31d-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd31d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd31d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd31d-135">-WhatIf</span></span>
<span data-ttu-id="cd31d-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd31d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd31d-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cd31d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd31d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd31d-138">CommonParameters</span></span>
<span data-ttu-id="cd31d-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd31d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd31d-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd31d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd31d-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd31d-141">INPUTS</span></span>

### <span data-ttu-id="cd31d-142">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="cd31d-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="cd31d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="cd31d-143">System.String</span></span>

## <span data-ttu-id="cd31d-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd31d-144">OUTPUTS</span></span>

### <span data-ttu-id="cd31d-145">System. String</span><span class="sxs-lookup"><span data-stu-id="cd31d-145">System.String</span></span>

## <span data-ttu-id="cd31d-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd31d-146">NOTES</span></span>

## <span data-ttu-id="cd31d-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd31d-147">RELATED LINKS</span></span>
