---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 91e4ec27298fa3fead3041e43f988b96ecf64046
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277100"
---
# <span data-ttu-id="d45f9-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="d45f9-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="d45f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d45f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d45f9-103">Yönetilen kümenin panosuna bir Kubectl SSH tüneli oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d45f9-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="d45f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d45f9-104">SYNTAX</span></span>

### <span data-ttu-id="d45f9-105">GroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d45f9-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-ListenPort <Int32>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d45f9-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="d45f9-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d45f9-107">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="d45f9-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d45f9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d45f9-108">DESCRIPTION</span></span>
<span data-ttu-id="d45f9-109">Yönetilen kümenin panosuna bir Kubectl SSH tüneli oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d45f9-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="d45f9-110">SSH tüneli Kubectl-Tunnel adındaki bir PowerShell işinde ayarlanır ve çalışır `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="d45f9-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="d45f9-111">Tünelin üzerinden erişilebilir olması gerekir [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="d45f9-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="d45f9-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d45f9-112">EXAMPLES</span></span>

### <span data-ttu-id="d45f9-113">Bir SSH tüneli başlatın ve bir tarayıcıyı Kubernetes panosuna açın</span><span class="sxs-lookup"><span data-stu-id="d45f9-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="d45f9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d45f9-114">PARAMETERS</span></span>

### <span data-ttu-id="d45f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d45f9-115">-DefaultProfile</span></span>
<span data-ttu-id="d45f9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d45f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d45f9-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="d45f9-117">-DisableBrowser</span></span>
<span data-ttu-id="d45f9-118">Kubectl bağlantı noktasını yükledikten sonra bir tarayıcı açın.</span><span class="sxs-lookup"><span data-stu-id="d45f9-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="d45f9-119">-ID</span><span class="sxs-lookup"><span data-stu-id="d45f9-119">-Id</span></span>
<span data-ttu-id="d45f9-120">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="d45f9-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="d45f9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d45f9-121">-InputObject</span></span>
<span data-ttu-id="d45f9-122">Normalde ardışık düzen aracılığıyla iletilen bir PSKubernetesCluster nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d45f9-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="d45f9-123">-ListenPort</span><span class="sxs-lookup"><span data-stu-id="d45f9-123">-ListenPort</span></span>
<span data-ttu-id="d45f9-124">Panonun dinleme bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="d45f9-124">The listening port for the dashboard.</span></span> <span data-ttu-id="d45f9-125">Varsayılan değer 8003 ' dır.</span><span class="sxs-lookup"><span data-stu-id="d45f9-125">Default value is 8003.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45f9-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="d45f9-126">-Name</span></span>
<span data-ttu-id="d45f9-127">Yönetilen Kubernetes kümeniz adı</span><span class="sxs-lookup"><span data-stu-id="d45f9-127">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="d45f9-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d45f9-128">-PassThru</span></span>
<span data-ttu-id="d45f9-129">Cmdlet, geçmişse, KubeTunnelJob öğesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d45f9-129">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="d45f9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d45f9-130">-ResourceGroupName</span></span>
<span data-ttu-id="d45f9-131">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d45f9-131">Resource group name</span></span>

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

### <span data-ttu-id="d45f9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d45f9-132">CommonParameters</span></span>
<span data-ttu-id="d45f9-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d45f9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d45f9-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d45f9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d45f9-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d45f9-135">INPUTS</span></span>

### <span data-ttu-id="d45f9-136">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="d45f9-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="d45f9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d45f9-137">System.String</span></span>

## <span data-ttu-id="d45f9-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d45f9-138">OUTPUTS</span></span>

### <span data-ttu-id="d45f9-139">Microsoft. Azure. Commands. aks. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="d45f9-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="d45f9-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d45f9-140">NOTES</span></span>

## <span data-ttu-id="d45f9-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d45f9-141">RELATED LINKS</span></span>
