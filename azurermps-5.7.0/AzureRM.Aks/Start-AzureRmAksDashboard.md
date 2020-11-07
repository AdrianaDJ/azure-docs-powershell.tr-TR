---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/start-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
ms.openlocfilehash: 5858a1f17bcae3c003ed7b40200c065c36eb2b1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763296"
---
# <span data-ttu-id="9e602-101">Start-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="9e602-101">Start-AzureRmAksDashboard</span></span>

## <span data-ttu-id="9e602-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e602-102">SYNOPSIS</span></span>
<span data-ttu-id="9e602-103">Yönetilen kümenin panosuna bir Kubectl SSH tüneli oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9e602-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e602-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e602-104">SYNTAX</span></span>

### <span data-ttu-id="9e602-105">GroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9e602-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzureRmAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e602-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="9e602-106">InputObjectParameterSet</span></span>
```
Start-AzureRmAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e602-107">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="9e602-107">IdParameterSet</span></span>
```
Start-AzureRmAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e602-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e602-108">DESCRIPTION</span></span>
<span data-ttu-id="9e602-109">Yönetilen kümenin panosuna bir Kubectl SSH tüneli oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9e602-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="9e602-110">SSH tüneli Kubectl-Tunnel adındaki bir PowerShell işinde ayarlanır ve çalışır `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="9e602-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="9e602-111">Tünele görüşmelidir [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="9e602-111">The tunnel should be accessable via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="9e602-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e602-112">EXAMPLES</span></span>

### <span data-ttu-id="9e602-113">Bir SSH tüneli başlatın ve bir tarayıcıyı Kubernetes panosuna açın</span><span class="sxs-lookup"><span data-stu-id="9e602-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzureRmAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="9e602-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e602-114">PARAMETERS</span></span>

### <span data-ttu-id="9e602-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e602-115">-DefaultProfile</span></span>
<span data-ttu-id="9e602-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e602-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e602-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="9e602-117">-DisableBrowser</span></span>
<span data-ttu-id="9e602-118">Establising kubectl bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="9e602-118">Do not pop open a browser after establising the kubectl port-forward.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e602-119">-ID</span><span class="sxs-lookup"><span data-stu-id="9e602-119">-Id</span></span>
<span data-ttu-id="9e602-120">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="9e602-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e602-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e602-121">-InputObject</span></span>
<span data-ttu-id="9e602-122">Normalde ardışık düzen aracılığıyla iletilen bir PSKubernetesCluster nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9e602-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e602-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="9e602-123">-Name</span></span>
<span data-ttu-id="9e602-124">Yönetilen Kubernetes kümeniz adı</span><span class="sxs-lookup"><span data-stu-id="9e602-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e602-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9e602-125">-PassThru</span></span>
<span data-ttu-id="9e602-126">Cmdlet, geçmişse, KubeTunnelJob öğesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9e602-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e602-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e602-127">-ResourceGroupName</span></span>
<span data-ttu-id="9e602-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="9e602-128">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e602-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e602-129">CommonParameters</span></span>
<span data-ttu-id="9e602-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e602-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e602-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e602-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e602-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e602-132">INPUTS</span></span>

### <span data-ttu-id="9e602-133">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="9e602-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="9e602-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9e602-134">System.String</span></span>

## <span data-ttu-id="9e602-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e602-135">OUTPUTS</span></span>

### <span data-ttu-id="9e602-136">Microsoft. Azure. Commands. aks. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="9e602-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="9e602-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e602-137">NOTES</span></span>

## <span data-ttu-id="9e602-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e602-138">RELATED LINKS</span></span>
