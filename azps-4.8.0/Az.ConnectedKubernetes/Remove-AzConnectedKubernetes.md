---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 4bc5c82bbfb930484a4a3541e7e97b68ce9be2e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266639"
---
# <span data-ttu-id="1197e-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="1197e-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="1197e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1197e-102">SYNOPSIS</span></span>
<span data-ttu-id="1197e-103">Azure Resource Manager 'da izlenen kaynağı kaldırarak bağlı kümeyi silin (ARM).</span><span class="sxs-lookup"><span data-stu-id="1197e-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="1197e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1197e-104">SYNTAX</span></span>

### <span data-ttu-id="1197e-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1197e-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1197e-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="1197e-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1197e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1197e-107">DESCRIPTION</span></span>
<span data-ttu-id="1197e-108">Azure Resource Manager 'da izlenen kaynağı kaldırarak bağlı kümeyi silin (ARM).</span><span class="sxs-lookup"><span data-stu-id="1197e-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="1197e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1197e-109">EXAMPLES</span></span>

### <span data-ttu-id="1197e-110">Örnek 1: bağlı kubererleri kaldırma</span><span class="sxs-lookup"><span data-stu-id="1197e-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="1197e-111">Bu komut bağlı bir kuberererleri kaldırır</span><span class="sxs-lookup"><span data-stu-id="1197e-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="1197e-112">Örnek 2: bağlı kubererleri nesneye göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="1197e-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="1197e-113">Bu komut, bağlı bir kubererleri nesneye göre kaldırır</span><span class="sxs-lookup"><span data-stu-id="1197e-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="1197e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1197e-114">PARAMETERS</span></span>

### <span data-ttu-id="1197e-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="1197e-115">-AsJob</span></span>
<span data-ttu-id="1197e-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="1197e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1197e-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1197e-117">-ClusterName</span></span>
<span data-ttu-id="1197e-118">Almanın çağrıldığı Kubernetes kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="1197e-118">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1197e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1197e-119">-DefaultProfile</span></span>
<span data-ttu-id="1197e-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1197e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1197e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1197e-121">-InputObject</span></span>
<span data-ttu-id="1197e-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1197e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1197e-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="1197e-123">-KubeConfig</span></span>
<span data-ttu-id="1197e-124">Kuto yapılandırma dosyasının yolu</span><span class="sxs-lookup"><span data-stu-id="1197e-124">Path to the kube config file</span></span>

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

### <span data-ttu-id="1197e-125">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="1197e-125">-KubeContext</span></span>
<span data-ttu-id="1197e-126">Geçerli makineden kubconfig bağlamı</span><span class="sxs-lookup"><span data-stu-id="1197e-126">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="1197e-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1197e-127">-NoWait</span></span>
<span data-ttu-id="1197e-128">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="1197e-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1197e-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1197e-129">-PassThru</span></span>
<span data-ttu-id="1197e-130">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="1197e-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1197e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1197e-131">-ResourceGroupName</span></span>
<span data-ttu-id="1197e-132">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1197e-132">The name of the resource group.</span></span>
<span data-ttu-id="1197e-133">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="1197e-133">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1197e-134">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1197e-134">-SubscriptionId</span></span>
<span data-ttu-id="1197e-135">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1197e-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1197e-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="1197e-136">-Confirm</span></span>
<span data-ttu-id="1197e-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1197e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1197e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1197e-138">-WhatIf</span></span>
<span data-ttu-id="1197e-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1197e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1197e-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1197e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1197e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1197e-141">CommonParameters</span></span>
<span data-ttu-id="1197e-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1197e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1197e-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1197e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1197e-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1197e-144">INPUTS</span></span>

### <span data-ttu-id="1197e-145">Microsoft. Azure. PowerShell. cmdlet. ConnectedKubernetes. modeller. Iconnectedkubernetesıdentity</span><span class="sxs-lookup"><span data-stu-id="1197e-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="1197e-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1197e-146">OUTPUTS</span></span>

### <span data-ttu-id="1197e-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1197e-147">System.Boolean</span></span>

## <span data-ttu-id="1197e-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1197e-148">NOTES</span></span>

<span data-ttu-id="1197e-149">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="1197e-149">ALIASES</span></span>

<span data-ttu-id="1197e-150">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="1197e-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1197e-151">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1197e-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1197e-152">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1197e-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1197e-153">INPUTOBJECT <IConnectedKubernetesIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="1197e-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1197e-154">`[ClusterName <String>]`: Get 'in çağrıldığı Kubernetes kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="1197e-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="1197e-155">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="1197e-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1197e-156">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1197e-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1197e-157">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="1197e-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="1197e-158">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1197e-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="1197e-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1197e-159">RELATED LINKS</span></span>

