---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: cc887fb8e41fd9464914144e7cbed5a332948228
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277192"
---
# <span data-ttu-id="9d687-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="9d687-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="9d687-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d687-102">SYNOPSIS</span></span>
<span data-ttu-id="9d687-103">Unregister-AzStackHCI, şirket içi kümeyi temsil eden Microsoft. AzureStackHCI bulut kaynağını silip şirket içi kümenin Azure ile kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="9d687-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="9d687-104">Hiçbir parametre geçirilmemişse kümenin kaydını kaldırmak için, kümedeki kullanılabilir olan kayıt bilgileri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9d687-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="9d687-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9d687-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d687-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d687-106">DESCRIPTION</span></span>
<span data-ttu-id="9d687-107">Unregister-AzStackHCI, şirket içi kümeyi temsil eden Microsoft. AzureStackHCI bulut kaynağını silip şirket içi kümenin Azure ile kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="9d687-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="9d687-108">Hiçbir parametre geçirilmemişse kümenin kaydını kaldırmak için, kümedeki kullanılabilir olan kayıt bilgileri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9d687-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="9d687-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9d687-109">EXAMPLES</span></span>

### <span data-ttu-id="9d687-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="9d687-110">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node
```

<span data-ttu-id="9d687-111">C:\PS \> Unregister-AzStackHCI sonucu: başarı</span><span class="sxs-lookup"><span data-stu-id="9d687-111">C:\PS\>Unregister-AzStackHCI Result: Success</span></span>

### <span data-ttu-id="9d687-112">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="9d687-112">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="9d687-113">C:\PS \> Unregister-AzStackHCI-ComputerName ClusterNode1 sonucu: başarı</span><span class="sxs-lookup"><span data-stu-id="9d687-113">C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span></span>

### <span data-ttu-id="9d687-114">ÖRNEK 3</span><span class="sxs-lookup"><span data-stu-id="9d687-114">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="9d687-115">C:\PS \> Unregister-Azstackhcı-SubscriptionID "12a0f531-56cb-4340-9501-257726vseç741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken.. rerrer-AccountID user1@corp1.com -resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG-confirm: $false sonucu: başarı</span><span class="sxs-lookup"><span data-stu-id="9d687-115">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span></span>

### <span data-ttu-id="9d687-116">ÖRNEK 4</span><span class="sxs-lookup"><span data-stu-id="9d687-116">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="9d687-117">C:\PS \> kaydını-AzStackHCI-SubscriptionID "12a0f531-56cb-4340-9501-257726vseç741fd"-resourceName HciCluster1-tenan"c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ... rerrer-AccountID user1@corp1.com -environmentname Azurecsesli-ComputerName node1hci-Credential Get-Credential Result: Success</span><span class="sxs-lookup"><span data-stu-id="9d687-117">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span></span>

## <span data-ttu-id="9d687-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9d687-118">PARAMETERS</span></span>

### <span data-ttu-id="9d687-119">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="9d687-119">-SubscriptionId</span></span>
<span data-ttu-id="9d687-120">Kaynağı oluşturmak için Azure aboneliğini belirtir</span><span class="sxs-lookup"><span data-stu-id="9d687-120">Specifies the Azure Subscription to create the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d687-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9d687-121">-ResourceName</span></span>
<span data-ttu-id="9d687-122">Azure 'da oluşturulan kaynağın kaynak adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d687-122">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="9d687-123">Belirtilmemişse, şirket içi küme adı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9d687-123">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d687-124">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="9d687-124">-TenantId</span></span>
<span data-ttu-id="9d687-125">Azure Tenantıd 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d687-125">Specifies the Azure TenantId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d687-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d687-126">-ResourceGroupName</span></span>
<span data-ttu-id="9d687-127">Azure Resource grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d687-127">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="9d687-128">Belirtilmemişse \<LocalClusterName\> -RG kaynak grubu adı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9d687-128">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d687-129">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="9d687-129">-ArmAccessToken</span></span>
<span data-ttu-id="9d687-130">ARM erişim belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d687-130">Specifies the ARM access token.</span></span>
<span data-ttu-id="9d687-131">GraphAccessToken ve AccountID ile birlikte bunu belirtmek için Azure etkileşimli oturum açma önlenir.</span><span class="sxs-lookup"><span data-stu-id="9d687-131">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d687-132">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="9d687-132">-GraphAccessToken</span></span>
<span data-ttu-id="9d687-133">Grafik erişim belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d687-133">Specifies the Graph access token.</span></span>
<span data-ttu-id="9d687-134">ArmAccessToken ve AccountID ile birlikte belirtmek için Azure etkileşimli oturum açma önlenir.</span><span class="sxs-lookup"><span data-stu-id="9d687-134">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d687-135">-AccountId</span><span class="sxs-lookup"><span data-stu-id="9d687-135">-AccountId</span></span>
<span data-ttu-id="9d687-136">ARM erişim belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d687-136">Specifies the ARM access token.</span></span>
<span data-ttu-id="9d687-137">ArmAccessToken ve GraphAccessToken ile birlikte belirtmek için Azure etkileşimli oturum açma önlenir.</span><span class="sxs-lookup"><span data-stu-id="9d687-137">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d687-138">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="9d687-138">-EnvironmentName</span></span>
<span data-ttu-id="9d687-139">Azure ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d687-139">Specifies the Azure Environment.</span></span>
<span data-ttu-id="9d687-140">Varsayılan olarak Azurecyüksek.</span><span class="sxs-lookup"><span data-stu-id="9d687-140">Default is AzureCloud.</span></span>
<span data-ttu-id="9d687-141">Geçerli değerler Azurecyüksek, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="9d687-141">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d687-142">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="9d687-142">-ComputerName</span></span>
<span data-ttu-id="9d687-143">Azure 'a kaydolan şirket içi kümesindeki küme düğümünden birini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d687-143">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d687-144">-Credential</span><span class="sxs-lookup"><span data-stu-id="9d687-144">-Credential</span></span>
<span data-ttu-id="9d687-145">ComputerName kimlik bilgisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d687-145">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="9d687-146">Varsayılan, cmdlet 'ı yürüten geçerli kullanıcıdır.</span><span class="sxs-lookup"><span data-stu-id="9d687-146">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d687-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d687-147">-WhatIf</span></span>
<span data-ttu-id="9d687-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9d687-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d687-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9d687-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d687-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="9d687-150">-Confirm</span></span>
<span data-ttu-id="9d687-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9d687-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d687-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d687-152">CommonParameters</span></span>
<span data-ttu-id="9d687-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9d687-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d687-154">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9d687-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d687-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9d687-155">INPUTS</span></span>

## <span data-ttu-id="9d687-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9d687-156">OUTPUTS</span></span>

### <span data-ttu-id="9d687-157">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="9d687-157">PSCustomObject.</span></span> <span data-ttu-id="9d687-158">PSCustomObject 'de aşağıdaki özellikleri döndürür</span><span class="sxs-lookup"><span data-stu-id="9d687-158">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="9d687-159">Sonuç: başarılı veya başarısız oldu ya da Iptal edildi.</span><span class="sxs-lookup"><span data-stu-id="9d687-159">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="9d687-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9d687-160">NOTES</span></span>

## <span data-ttu-id="9d687-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9d687-161">RELATED LINKS</span></span>
