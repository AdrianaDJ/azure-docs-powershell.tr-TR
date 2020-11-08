---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107469"
---
# <span data-ttu-id="741ff-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="741ff-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="741ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="741ff-102">SYNOPSIS</span></span>
<span data-ttu-id="741ff-103">SYNAPSE Analytics güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="741ff-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="741ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="741ff-104">SYNTAX</span></span>

### <span data-ttu-id="741ff-105">CreateByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="741ff-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="741ff-106">Createbynameallowtalpparameterset</span><span class="sxs-lookup"><span data-stu-id="741ff-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="741ff-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="741ff-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="741ff-108">Createbyparentobjectallowtalpparameterset</span><span class="sxs-lookup"><span data-stu-id="741ff-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="741ff-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="741ff-109">DESCRIPTION</span></span>
<span data-ttu-id="741ff-110">**New-AzSynapseFirewallRule** cmdlet 'ı bir Azure SYNAPSE Analytics güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="741ff-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="741ff-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="741ff-111">EXAMPLES</span></span>

### <span data-ttu-id="741ff-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="741ff-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="741ff-113">Bu komut ContosoFirewallRule adlı bir güvenlik duvarı kuralı çalışma alanı adı ContosoFirewallRule ile oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="741ff-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="741ff-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="741ff-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="741ff-115">Bu komut, ardışık düzen aracılığıyla ContosoFirewallRule adlı güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="741ff-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="741ff-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="741ff-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="741ff-117">Bu komut, bir çalışma alanı altındaki tüm Azure IP 'lerinin bulunduğu güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="741ff-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="741ff-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="741ff-118">PARAMETERS</span></span>

### <span data-ttu-id="741ff-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="741ff-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="741ff-120">Tüm Azure IP 'Lerinin erişimine izin veren özel bir güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="741ff-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateByNameAllowAllIpParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="741ff-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="741ff-121">-AsJob</span></span>
<span data-ttu-id="741ff-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="741ff-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="741ff-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="741ff-123">-DefaultProfile</span></span>
<span data-ttu-id="741ff-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="741ff-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="741ff-125">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="741ff-125">-EndIpAddress</span></span>
<span data-ttu-id="741ff-126">Güvenlik duvarı kuralının bitiş IP adresi.</span><span class="sxs-lookup"><span data-stu-id="741ff-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="741ff-127">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="741ff-127">Must be IPv4 format.</span></span>
<span data-ttu-id="741ff-128">Startıpaddress 'den büyük veya buna eşit olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="741ff-128">Must be greater than or equal to startIpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="741ff-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="741ff-129">-Name</span></span>
<span data-ttu-id="741ff-130">Çalışma alanı için firerduvar kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="741ff-130">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="741ff-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="741ff-131">-ResourceGroupName</span></span>
<span data-ttu-id="741ff-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="741ff-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="741ff-133">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="741ff-133">-StartIpAddress</span></span>
<span data-ttu-id="741ff-134">Güvenlik duvarı kuralının başlangıç IP adresi.</span><span class="sxs-lookup"><span data-stu-id="741ff-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="741ff-135">IPv4 biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="741ff-135">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="741ff-136">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="741ff-136">-WorkspaceName</span></span>
<span data-ttu-id="741ff-137">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="741ff-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="741ff-138">-</span><span class="sxs-lookup"><span data-stu-id="741ff-138">-WorkspaceObject</span></span>
<span data-ttu-id="741ff-139">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="741ff-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="741ff-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="741ff-140">-Confirm</span></span>
<span data-ttu-id="741ff-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="741ff-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="741ff-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="741ff-142">-WhatIf</span></span>
<span data-ttu-id="741ff-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="741ff-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="741ff-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="741ff-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="741ff-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="741ff-145">CommonParameters</span></span>
<span data-ttu-id="741ff-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="741ff-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="741ff-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="741ff-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="741ff-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="741ff-148">INPUTS</span></span>

### <span data-ttu-id="741ff-149">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="741ff-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="741ff-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="741ff-150">OUTPUTS</span></span>

### <span data-ttu-id="741ff-151">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="741ff-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="741ff-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="741ff-152">NOTES</span></span>

## <span data-ttu-id="741ff-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="741ff-153">RELATED LINKS</span></span>
