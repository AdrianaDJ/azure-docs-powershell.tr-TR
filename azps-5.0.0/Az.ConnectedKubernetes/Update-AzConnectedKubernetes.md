---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2913a4288bad6c1cb8c908d80b8c751a08483a8b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276750"
---
# <span data-ttu-id="642a7-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="642a7-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="642a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="642a7-102">SYNOPSIS</span></span>
<span data-ttu-id="642a7-103">Bağlı küme kaynağının belirli özelliklerini güncelleştiren API</span><span class="sxs-lookup"><span data-stu-id="642a7-103">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="642a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="642a7-104">SYNTAX</span></span>

### <span data-ttu-id="642a7-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="642a7-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="642a7-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="642a7-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="642a7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="642a7-107">DESCRIPTION</span></span>
<span data-ttu-id="642a7-108">Bağlı küme kaynağının belirli özelliklerini güncelleştiren API</span><span class="sxs-lookup"><span data-stu-id="642a7-108">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="642a7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="642a7-109">EXAMPLES</span></span>

### <span data-ttu-id="642a7-110">Örnek 1: bağlı kubererleri güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="642a7-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="642a7-111">Bu komut, bağlı bir kuberneika 'ı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="642a7-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="642a7-112">Örnek 2: bağlantılı bir kubererleri nesneye göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="642a7-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="642a7-113">Bu komut, bağlı bir kubererleri nesneye göre güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="642a7-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="642a7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="642a7-114">PARAMETERS</span></span>

### <span data-ttu-id="642a7-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="642a7-115">-ClusterName</span></span>
<span data-ttu-id="642a7-116">Almanın çağrıldığı Kubernetes kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="642a7-116">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="642a7-117">-DefaultProfile</span></span>
<span data-ttu-id="642a7-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="642a7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="642a7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="642a7-119">-InputObject</span></span>
<span data-ttu-id="642a7-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="642a7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="642a7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="642a7-121">-ResourceGroupName</span></span>
<span data-ttu-id="642a7-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="642a7-122">The name of the resource group.</span></span>
<span data-ttu-id="642a7-123">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="642a7-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642a7-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="642a7-124">-SubscriptionId</span></span>
<span data-ttu-id="642a7-125">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="642a7-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642a7-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="642a7-126">-Tag</span></span>
<span data-ttu-id="642a7-127">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="642a7-127">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642a7-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="642a7-128">-Confirm</span></span>
<span data-ttu-id="642a7-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="642a7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="642a7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="642a7-130">-WhatIf</span></span>
<span data-ttu-id="642a7-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="642a7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="642a7-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="642a7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="642a7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="642a7-133">CommonParameters</span></span>
<span data-ttu-id="642a7-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="642a7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="642a7-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="642a7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="642a7-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="642a7-136">INPUTS</span></span>

### <span data-ttu-id="642a7-137">Microsoft. Azure. PowerShell. cmdlet. ConnectedKubernetes. modeller. Iconnectedkubernetesıdentity</span><span class="sxs-lookup"><span data-stu-id="642a7-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="642a7-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="642a7-138">OUTPUTS</span></span>

### <span data-ttu-id="642a7-139">Microsoft. Azure. PowerShell. cmdlet. ConnectedKubernetes. modeller. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="642a7-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="642a7-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="642a7-140">NOTES</span></span>

<span data-ttu-id="642a7-141">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="642a7-141">ALIASES</span></span>

<span data-ttu-id="642a7-142">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="642a7-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="642a7-143">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="642a7-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="642a7-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="642a7-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="642a7-145">INPUTOBJECT <IConnectedKubernetesIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="642a7-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="642a7-146">`[ClusterName <String>]`: Get 'in çağrıldığı Kubernetes kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="642a7-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="642a7-147">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="642a7-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="642a7-148">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="642a7-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="642a7-149">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="642a7-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="642a7-150">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="642a7-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="642a7-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="642a7-151">RELATED LINKS</span></span>

