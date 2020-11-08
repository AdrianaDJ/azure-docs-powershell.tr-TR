---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: 1df844fc9a040fe20b6fdcdaa6f5dccda191aba4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268874"
---
# <span data-ttu-id="8704b-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="8704b-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="8704b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8704b-102">SYNOPSIS</span></span>
<span data-ttu-id="8704b-103">Ad, kimlik, Özellikler ve ek küme ayrıntıları da içinde olmak üzere, belirtilen bağlı kümenin özelliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8704b-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="8704b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8704b-104">SYNTAX</span></span>

### <span data-ttu-id="8704b-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8704b-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8704b-106">Al</span><span class="sxs-lookup"><span data-stu-id="8704b-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8704b-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="8704b-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8704b-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="8704b-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8704b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="8704b-109">DESCRIPTION</span></span>
<span data-ttu-id="8704b-110">Ad, kimlik, Özellikler ve ek küme ayrıntıları da içinde olmak üzere, belirtilen bağlı kümenin özelliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8704b-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="8704b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8704b-111">EXAMPLES</span></span>

### <span data-ttu-id="8704b-112">Örnek 1: aboneliğin altındaki tüm bağlı kererleri alma</span><span class="sxs-lookup"><span data-stu-id="8704b-112">Example 1: Get all connected kubernetes under a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="8704b-113">Bu komut, bir aboneliğin altındaki tüm bağlı kuberleri alır.</span><span class="sxs-lookup"><span data-stu-id="8704b-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="8704b-114">Örnek 2: kaynak grubu altındaki tüm bağlı kuberleri alma</span><span class="sxs-lookup"><span data-stu-id="8704b-114">Example 2: Get all connected kubernetes under the resource group</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="8704b-115">Bu komut, kaynak grubu altındaki tüm bağlı kuberleri alır.</span><span class="sxs-lookup"><span data-stu-id="8704b-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="8704b-116">Örnek 3: bağlantı</span><span class="sxs-lookup"><span data-stu-id="8704b-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="8704b-117">Bu komut, bağlı kubererleri alır.</span><span class="sxs-lookup"><span data-stu-id="8704b-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="8704b-118">Örnek 4: nesneye göre bağlı bir kuberertes alma</span><span class="sxs-lookup"><span data-stu-id="8704b-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="8704b-119">Bu komut, bağlı bir kubererleri nesneye göre alır.</span><span class="sxs-lookup"><span data-stu-id="8704b-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="8704b-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8704b-120">PARAMETERS</span></span>

### <span data-ttu-id="8704b-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8704b-121">-ClusterName</span></span>
<span data-ttu-id="8704b-122">Almanın çağrıldığı Kubernetes kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="8704b-122">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8704b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8704b-123">-DefaultProfile</span></span>
<span data-ttu-id="8704b-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8704b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8704b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8704b-125">-InputObject</span></span>
<span data-ttu-id="8704b-126">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8704b-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8704b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8704b-127">-ResourceGroupName</span></span>
<span data-ttu-id="8704b-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8704b-128">The name of the resource group.</span></span>
<span data-ttu-id="8704b-129">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="8704b-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8704b-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="8704b-130">-SubscriptionId</span></span>
<span data-ttu-id="8704b-131">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8704b-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8704b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8704b-132">CommonParameters</span></span>
<span data-ttu-id="8704b-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8704b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8704b-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8704b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8704b-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8704b-135">INPUTS</span></span>

### <span data-ttu-id="8704b-136">Microsoft. Azure. PowerShell. cmdlet. ConnectedKubernetes. modeller. Iconnectedkubernetesıdentity</span><span class="sxs-lookup"><span data-stu-id="8704b-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="8704b-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8704b-137">OUTPUTS</span></span>

### <span data-ttu-id="8704b-138">Microsoft. Azure. PowerShell. cmdlet. ConnectedKubernetes. modeller. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="8704b-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="8704b-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8704b-139">NOTES</span></span>

<span data-ttu-id="8704b-140">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="8704b-140">ALIASES</span></span>

<span data-ttu-id="8704b-141">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="8704b-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8704b-142">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8704b-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8704b-143">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8704b-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8704b-144">INPUTOBJECT <IConnectedKubernetesIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="8704b-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8704b-145">`[ClusterName <String>]`: Get 'in çağrıldığı Kubernetes kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="8704b-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="8704b-146">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="8704b-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8704b-147">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8704b-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8704b-148">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="8704b-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="8704b-149">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8704b-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="8704b-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8704b-150">RELATED LINKS</span></span>

