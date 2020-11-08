---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 5a03df969421ea87d907efb5fe23027acfde0834
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096691"
---
# <span data-ttu-id="02682-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="02682-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="02682-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02682-102">SYNOPSIS</span></span>
<span data-ttu-id="02682-103">Yönetilen kümenin panosuna bir Kubectl SSH tüneli oluşturun.</span><span class="sxs-lookup"><span data-stu-id="02682-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="02682-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02682-104">SYNTAX</span></span>

### <span data-ttu-id="02682-105">GroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="02682-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02682-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="02682-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02682-107">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="02682-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02682-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="02682-108">DESCRIPTION</span></span>
<span data-ttu-id="02682-109">Yönetilen kümenin panosuna bir Kubectl SSH tüneli oluşturun.</span><span class="sxs-lookup"><span data-stu-id="02682-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="02682-110">SSH tüneli Kubectl-Tunnel adındaki bir PowerShell işinde ayarlanır ve çalışır `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="02682-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="02682-111">Tünelin üzerinden erişilebilir olması gerekir [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="02682-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="02682-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02682-112">EXAMPLES</span></span>

### <span data-ttu-id="02682-113">Bir SSH tüneli başlatın ve bir tarayıcıyı Kubernetes panosuna açın</span><span class="sxs-lookup"><span data-stu-id="02682-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="02682-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02682-114">PARAMETERS</span></span>

### <span data-ttu-id="02682-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02682-115">-DefaultProfile</span></span>
<span data-ttu-id="02682-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02682-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02682-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="02682-117">-DisableBrowser</span></span>
<span data-ttu-id="02682-118">Kubectl bağlantı noktasını yükledikten sonra bir tarayıcı açın.</span><span class="sxs-lookup"><span data-stu-id="02682-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="02682-119">-ID</span><span class="sxs-lookup"><span data-stu-id="02682-119">-Id</span></span>
<span data-ttu-id="02682-120">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="02682-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="02682-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02682-121">-InputObject</span></span>
<span data-ttu-id="02682-122">Normalde ardışık düzen aracılığıyla iletilen bir PSKubernetesCluster nesnesi.</span><span class="sxs-lookup"><span data-stu-id="02682-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02682-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="02682-123">-Name</span></span>
<span data-ttu-id="02682-124">Yönetilen Kubernetes kümeniz adı</span><span class="sxs-lookup"><span data-stu-id="02682-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="02682-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="02682-125">-PassThru</span></span>
<span data-ttu-id="02682-126">Cmdlet, geçmişse, KubeTunnelJob öğesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="02682-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="02682-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02682-127">-ResourceGroupName</span></span>
<span data-ttu-id="02682-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="02682-128">Resource group name</span></span>

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

### <span data-ttu-id="02682-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02682-129">CommonParameters</span></span>
<span data-ttu-id="02682-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02682-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02682-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02682-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02682-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02682-132">INPUTS</span></span>

### <span data-ttu-id="02682-133">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="02682-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="02682-134">System. String</span><span class="sxs-lookup"><span data-stu-id="02682-134">System.String</span></span>

## <span data-ttu-id="02682-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02682-135">OUTPUTS</span></span>

### <span data-ttu-id="02682-136">Microsoft. Azure. Commands. aks. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="02682-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="02682-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02682-137">NOTES</span></span>

## <span data-ttu-id="02682-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02682-138">RELATED LINKS</span></span>
