---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: 09f1cd27e9af0c6442afa00d5301975cae8fbdeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320214"
---
# <span data-ttu-id="74a1b-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="74a1b-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="74a1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="74a1b-103">Yeni bir çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="74a1b-103">Creates a new workspace.</span></span>

## <span data-ttu-id="74a1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74a1b-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="74a1b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="74a1b-105">DESCRIPTION</span></span>
<span data-ttu-id="74a1b-106">Yeni bir çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="74a1b-106">Creates a new workspace.</span></span>

## <span data-ttu-id="74a1b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74a1b-107">EXAMPLES</span></span>

### <span data-ttu-id="74a1b-108">Örnek 1: Veriricks çalışma alanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="74a1b-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="74a1b-109">Bu komut, bir Veriricks çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="74a1b-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="74a1b-110">Örnek 2: özelleştirilmiş sanal ağ ile Veriricks çalışma alanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="74a1b-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
```powershell
PS C:\> $dlg = New-AzDelegation -Name dbrdl -ServiceName "Microsoft.Databricks/workspaces"
PS C:\> $rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName testgroup -Location eastus -Name nsg-test -SecurityRules $rdpRule
PS C:\> $privSubnet = New-AzVirtualNetworkSubnetConfig -Name priv-sub -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $pubSubnet = New-AzVirtualNetworkSubnetConfig -Name pub-sub  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $testVN = New-AzVirtualNetwork -Name testvn -ResourceGroupName testgroup -Location eastus -AddressPrefix "10.0.0.0/16" -Subnet $privSubnet,$pubSubnet
PS C:\> New-AzDatabricksWorkspace -Name databricks-test-with-custom-vn -ResourceGroupName testgroup -Location eastus -VirtualNetworkId $testVN.Id -PrivateSubnetName $privSubnet.Name -PublicSubnetName $privSubnet.Name -Sku standard

Location Name                           Type
-------- ----                           ----
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="74a1b-111">Bu komut, kaynak grubunda özelleştirilmiş sanal ağ içeren bir Veriricks çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="74a1b-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="74a1b-112">Örnek 3: şifrelemeyi etkinleştirme çalışma alanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="74a1b-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="74a1b-113">Bu komut, bir Veriricks çalışma alanı oluşturur ve şifrelemeyi hazırlamak üzere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="74a1b-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="74a1b-114">Daha fazla bilgi için lütfen Update-AzDatabricksWorkspace örneklerine bakın.</span><span class="sxs-lookup"><span data-stu-id="74a1b-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="74a1b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74a1b-115">PARAMETERS</span></span>

### <span data-ttu-id="74a1b-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="74a1b-116">-AsJob</span></span>
<span data-ttu-id="74a1b-117">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="74a1b-117">Run the command as a job</span></span>

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

### <span data-ttu-id="74a1b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a1b-118">-DefaultProfile</span></span>
<span data-ttu-id="74a1b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="74a1b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74a1b-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="74a1b-120">-Location</span></span>
<span data-ttu-id="74a1b-121">Kaynağın yaşadığı coğrafi konum</span><span class="sxs-lookup"><span data-stu-id="74a1b-121">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a1b-122">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74a1b-122">-ManagedResourceGroupName</span></span>
<span data-ttu-id="74a1b-123">Yönetilen kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="74a1b-123">The managed resource group name.</span></span>

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

### <span data-ttu-id="74a1b-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="74a1b-124">-Name</span></span>
<span data-ttu-id="74a1b-125">Çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="74a1b-125">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a1b-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="74a1b-126">-NoWait</span></span>
<span data-ttu-id="74a1b-127">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="74a1b-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="74a1b-128">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="74a1b-128">-PrepareEncryption</span></span>
<span data-ttu-id="74a1b-129">Çalışma alanını şifreleme için hazırlayın.</span><span class="sxs-lookup"><span data-stu-id="74a1b-129">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="74a1b-130">Yönetilen depolama hesabı için yönetilen kimliği etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="74a1b-130">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="74a1b-131">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="74a1b-131">-PrivateSubnetName</span></span>
<span data-ttu-id="74a1b-132">Sanal ağdaki özel alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="74a1b-132">The name of the Private Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="74a1b-133">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="74a1b-133">-PublicSubnetName</span></span>
<span data-ttu-id="74a1b-134">Sanal ağ içindeki genel alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="74a1b-134">The name of a Public Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="74a1b-135">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="74a1b-135">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="74a1b-136">DBFS kök dosya sisteminin, geri kalan veriler için platform yönetilen anahtarlarıyla, ikincil şifreleme katmanıyla etkinleştirilip etkinleştirilmeyeceğini belirten Boole değeri.</span><span class="sxs-lookup"><span data-stu-id="74a1b-136">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="74a1b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74a1b-137">-ResourceGroupName</span></span>
<span data-ttu-id="74a1b-138">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="74a1b-138">The name of the resource group.</span></span>
<span data-ttu-id="74a1b-139">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="74a1b-139">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a1b-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="74a1b-140">-Sku</span></span>
<span data-ttu-id="74a1b-141">SKU adı.</span><span class="sxs-lookup"><span data-stu-id="74a1b-141">The SKU name.</span></span>

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

### <span data-ttu-id="74a1b-142">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="74a1b-142">-SubscriptionId</span></span>
<span data-ttu-id="74a1b-143">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="74a1b-143">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a1b-144">Etiketli</span><span class="sxs-lookup"><span data-stu-id="74a1b-144">-Tag</span></span>
<span data-ttu-id="74a1b-145">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="74a1b-145">Resource tags.</span></span>

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

### <span data-ttu-id="74a1b-146">-Virtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="74a1b-146">-VirtualNetworkId</span></span>
<span data-ttu-id="74a1b-147">Bu Veriricks kümesinin oluşturulması gereken sanal ağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="74a1b-147">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

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

### <span data-ttu-id="74a1b-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="74a1b-148">-Confirm</span></span>
<span data-ttu-id="74a1b-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="74a1b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74a1b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74a1b-150">-WhatIf</span></span>
<span data-ttu-id="74a1b-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="74a1b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74a1b-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="74a1b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74a1b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a1b-153">CommonParameters</span></span>
<span data-ttu-id="74a1b-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74a1b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a1b-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="74a1b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a1b-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74a1b-156">INPUTS</span></span>

## <span data-ttu-id="74a1b-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74a1b-157">OUTPUTS</span></span>

### <span data-ttu-id="74a1b-158">Microsoft. Azure. PowerShell. cmdlet. Veriricks. modeller. Api20180401. ıworkspace</span><span class="sxs-lookup"><span data-stu-id="74a1b-158">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="74a1b-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74a1b-159">NOTES</span></span>

<span data-ttu-id="74a1b-160">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="74a1b-160">ALIASES</span></span>

## <span data-ttu-id="74a1b-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74a1b-161">RELATED LINKS</span></span>

