---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: 7f2bb3f1d378afec5b0774aec2977b507654b931
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320229"
---
# <span data-ttu-id="bfddc-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="bfddc-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="bfddc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfddc-102">SYNOPSIS</span></span>
<span data-ttu-id="bfddc-103">Çalışma alanını alır.</span><span class="sxs-lookup"><span data-stu-id="bfddc-103">Gets the workspace.</span></span>

## <span data-ttu-id="bfddc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bfddc-104">SYNTAX</span></span>

### <span data-ttu-id="bfddc-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bfddc-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bfddc-106">Al</span><span class="sxs-lookup"><span data-stu-id="bfddc-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bfddc-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="bfddc-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bfddc-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="bfddc-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="bfddc-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="bfddc-109">DESCRIPTION</span></span>
<span data-ttu-id="bfddc-110">Çalışma alanını alır.</span><span class="sxs-lookup"><span data-stu-id="bfddc-110">Gets the workspace.</span></span>

## <span data-ttu-id="bfddc-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bfddc-111">EXAMPLES</span></span>

### <span data-ttu-id="bfddc-112">Örnek 1: adla Veriricks çalışma alanı alma</span><span class="sxs-lookup"><span data-stu-id="bfddc-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="bfddc-113">Bu komut, kaynak grubundaki Veriricks çalışma alanını alır.</span><span class="sxs-lookup"><span data-stu-id="bfddc-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="bfddc-114">Örnek 2: bir abonelikteki tüm Veriricks çalışma alanlarını listeleyin</span><span class="sxs-lookup"><span data-stu-id="bfddc-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="bfddc-115">Bu komut, bir abonelikteki tüm veririci çalışma alanlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="bfddc-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="bfddc-116">Örnek 3: kaynak grubundaki tüm Veriricks çalışma alanlarını listeleyin</span><span class="sxs-lookup"><span data-stu-id="bfddc-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="bfddc-117">Bu komut, kaynak grubundaki tüm Veriricks çalışma alanlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="bfddc-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="bfddc-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bfddc-118">PARAMETERS</span></span>

### <span data-ttu-id="bfddc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfddc-119">-DefaultProfile</span></span>
<span data-ttu-id="bfddc-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bfddc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfddc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfddc-121">-InputObject</span></span>
<span data-ttu-id="bfddc-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bfddc-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfddc-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="bfddc-123">-Name</span></span>
<span data-ttu-id="bfddc-124">Çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="bfddc-124">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfddc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfddc-125">-ResourceGroupName</span></span>
<span data-ttu-id="bfddc-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bfddc-126">The name of the resource group.</span></span>
<span data-ttu-id="bfddc-127">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="bfddc-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bfddc-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="bfddc-128">-SubscriptionId</span></span>
<span data-ttu-id="bfddc-129">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bfddc-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bfddc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfddc-130">CommonParameters</span></span>
<span data-ttu-id="bfddc-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bfddc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfddc-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bfddc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfddc-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bfddc-133">INPUTS</span></span>

### <span data-ttu-id="bfddc-134">Microsoft. Azure. PowerShell. cmdlet. Veriricks. model. ıdatabricksıdentity</span><span class="sxs-lookup"><span data-stu-id="bfddc-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="bfddc-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bfddc-135">OUTPUTS</span></span>

### <span data-ttu-id="bfddc-136">Microsoft. Azure. PowerShell. cmdlet. Veriricks. modeller. Api20180401. ıworkspace</span><span class="sxs-lookup"><span data-stu-id="bfddc-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="bfddc-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bfddc-137">NOTES</span></span>

<span data-ttu-id="bfddc-138">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="bfddc-138">ALIASES</span></span>

<span data-ttu-id="bfddc-139">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="bfddc-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bfddc-140">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bfddc-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bfddc-141">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bfddc-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bfddc-142">INPUTOBJECT <IDatabricksIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="bfddc-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bfddc-143">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="bfddc-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bfddc-144">`[PeeringName <String>]`: Çalışma alanı vNet eşlemesi adı.</span><span class="sxs-lookup"><span data-stu-id="bfddc-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="bfddc-145">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bfddc-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bfddc-146">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="bfddc-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="bfddc-147">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bfddc-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bfddc-148">`[WorkspaceName <String>]`: Çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="bfddc-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="bfddc-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bfddc-149">RELATED LINKS</span></span>

