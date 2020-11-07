---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/import-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Import-AzureRmAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Import-AzureRmAksCredential.md
ms.openlocfilehash: b65ac736be5ee5f2f0592bcb2fdc84c873361f9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592358"
---
# <span data-ttu-id="a05b0-101">Import-AzureRmAksCredential</span><span class="sxs-lookup"><span data-stu-id="a05b0-101">Import-AzureRmAksCredential</span></span>

## <span data-ttu-id="a05b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a05b0-102">SYNOPSIS</span></span>
<span data-ttu-id="a05b0-103">Yönetilen Kubernetes kümesi için Kubectl yapılandırmasını içeri aktarın ve birleştirin.</span><span class="sxs-lookup"><span data-stu-id="a05b0-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a05b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a05b0-104">SYNTAX</span></span>

### <span data-ttu-id="a05b0-105">GroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a05b0-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzureRmAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a05b0-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="a05b0-106">InputObjectParameterSet</span></span>
```
Import-AzureRmAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a05b0-107">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="a05b0-107">IdParameterSet</span></span>
```
Import-AzureRmAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a05b0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a05b0-108">DESCRIPTION</span></span>
<span data-ttu-id="a05b0-109">Yönetilen Kubernetes kümesi için Kubectl yapılandırmasını içeri aktarın ve birleştirin.</span><span class="sxs-lookup"><span data-stu-id="a05b0-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="a05b0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a05b0-110">EXAMPLES</span></span>

### <span data-ttu-id="a05b0-111">Kubectl yapılandırmasını içeri ve birleştirme</span><span class="sxs-lookup"><span data-stu-id="a05b0-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzureRmAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="a05b0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a05b0-112">PARAMETERS</span></span>

### <span data-ttu-id="a05b0-113">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="a05b0-113">-Admin</span></span>
<span data-ttu-id="a05b0-114">Varsayılan ' clusterUser ' yerine ' clusterAdmin' kubectl config 'i alın.</span><span class="sxs-lookup"><span data-stu-id="a05b0-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="a05b0-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="a05b0-115">-ConfigPath</span></span>
<span data-ttu-id="a05b0-116">Oluşturulacak veya güncelleştirilecek bir kubectl yapılandırma dosyası.</span><span class="sxs-lookup"><span data-stu-id="a05b0-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="a05b0-117">Bunun yerine stdout ile</span><span class="sxs-lookup"><span data-stu-id="a05b0-117">Use '-' to print YAML to stdout instead.</span></span> <span data-ttu-id="a05b0-118">Varsayılan:% giriş%/.Kube/config.</span><span class="sxs-lookup"><span data-stu-id="a05b0-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="a05b0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a05b0-119">-DefaultProfile</span></span>
<span data-ttu-id="a05b0-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a05b0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a05b0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a05b0-121">-Force</span></span>
<span data-ttu-id="a05b0-122">Varsayılan olsa bile Kubernetes yapılandırmasını içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="a05b0-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="a05b0-123">-ID</span><span class="sxs-lookup"><span data-stu-id="a05b0-123">-Id</span></span>
<span data-ttu-id="a05b0-124">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="a05b0-124">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="a05b0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a05b0-125">-InputObject</span></span>
<span data-ttu-id="a05b0-126">Normalde ardışık düzen aracılığıyla iletilen bir PSKubernetesCluster nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a05b0-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="a05b0-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="a05b0-127">-Name</span></span>
<span data-ttu-id="a05b0-128">Yönetilen Kubernetes kümeniz adı</span><span class="sxs-lookup"><span data-stu-id="a05b0-128">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="a05b0-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a05b0-129">-PassThru</span></span>
<span data-ttu-id="a05b0-130">İçeri aktarma işlemi başarılıysa doğru verir</span><span class="sxs-lookup"><span data-stu-id="a05b0-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="a05b0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a05b0-131">-ResourceGroupName</span></span>
<span data-ttu-id="a05b0-132">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a05b0-132">Resource group name</span></span>

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

### <span data-ttu-id="a05b0-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="a05b0-133">-Confirm</span></span>
<span data-ttu-id="a05b0-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a05b0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a05b0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a05b0-135">-WhatIf</span></span>
<span data-ttu-id="a05b0-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a05b0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a05b0-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a05b0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a05b0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a05b0-138">CommonParameters</span></span>
<span data-ttu-id="a05b0-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a05b0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a05b0-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a05b0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a05b0-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a05b0-141">INPUTS</span></span>

### <span data-ttu-id="a05b0-142">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="a05b0-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="a05b0-143">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a05b0-143">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a05b0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a05b0-144">System.String</span></span>

## <span data-ttu-id="a05b0-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a05b0-145">OUTPUTS</span></span>

### <span data-ttu-id="a05b0-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a05b0-146">System.String</span></span>

## <span data-ttu-id="a05b0-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a05b0-147">NOTES</span></span>

## <span data-ttu-id="a05b0-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a05b0-148">RELATED LINKS</span></span>