---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/start-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
ms.openlocfilehash: 5258fc6685e57224b51c3be45c64191076136221
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278971"
---
# <span data-ttu-id="f8276-101">Start-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="f8276-101">Start-AzKustoCluster</span></span>

## <span data-ttu-id="f8276-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8276-102">SYNOPSIS</span></span>
<span data-ttu-id="f8276-103">Kusto kümesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="f8276-103">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="f8276-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8276-104">SYNTAX</span></span>

### <span data-ttu-id="f8276-105">Başlangıç (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f8276-105">Start (Default)</span></span>
```
Start-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f8276-106">Startviaıdentity</span><span class="sxs-lookup"><span data-stu-id="f8276-106">StartViaIdentity</span></span>
```
Start-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f8276-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8276-107">DESCRIPTION</span></span>
<span data-ttu-id="f8276-108">Kusto kümesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="f8276-108">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="f8276-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8276-109">EXAMPLES</span></span>

### <span data-ttu-id="f8276-110">Örnek 1: kusto kümesi başlatma</span><span class="sxs-lookup"><span data-stu-id="f8276-110">Example 1: Start a Kusto cluster</span></span>
```powershell
PS C:\> Start-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="f8276-111">Yukarıdaki komut kusto kümesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="f8276-111">The above command starts a Kusto cluster.</span></span>

## <span data-ttu-id="f8276-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8276-112">PARAMETERS</span></span>

### <span data-ttu-id="f8276-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="f8276-113">-AsJob</span></span>
<span data-ttu-id="f8276-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="f8276-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f8276-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8276-115">-DefaultProfile</span></span>
<span data-ttu-id="f8276-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f8276-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8276-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8276-117">-InputObject</span></span>
<span data-ttu-id="f8276-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8276-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8276-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="f8276-119">-Name</span></span>
<span data-ttu-id="f8276-120">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="f8276-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8276-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f8276-121">-NoWait</span></span>
<span data-ttu-id="f8276-122">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="f8276-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f8276-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f8276-123">-PassThru</span></span>
<span data-ttu-id="f8276-124">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="f8276-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f8276-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8276-125">-ResourceGroupName</span></span>
<span data-ttu-id="f8276-126">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f8276-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8276-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f8276-127">-SubscriptionId</span></span>
<span data-ttu-id="f8276-128">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="f8276-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f8276-129">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f8276-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8276-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="f8276-130">-Confirm</span></span>
<span data-ttu-id="f8276-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f8276-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8276-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8276-132">-WhatIf</span></span>
<span data-ttu-id="f8276-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f8276-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8276-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f8276-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8276-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8276-135">CommonParameters</span></span>
<span data-ttu-id="f8276-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8276-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8276-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f8276-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8276-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8276-138">INPUTS</span></span>

### <span data-ttu-id="f8276-139">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity</span><span class="sxs-lookup"><span data-stu-id="f8276-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f8276-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8276-140">OUTPUTS</span></span>

### <span data-ttu-id="f8276-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8276-141">System.Boolean</span></span>

## <span data-ttu-id="f8276-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8276-142">NOTES</span></span>

<span data-ttu-id="f8276-143">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="f8276-143">ALIASES</span></span>

<span data-ttu-id="f8276-144">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="f8276-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f8276-145">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f8276-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f8276-146">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f8276-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f8276-147">INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="f8276-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f8276-148">`[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="f8276-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f8276-149">`[ClusterName <String>]`: Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="f8276-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f8276-150">`[DataConnectionName <String>]`: Veri bağlantısının adı.</span><span class="sxs-lookup"><span data-stu-id="f8276-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f8276-151">`[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="f8276-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f8276-152">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="f8276-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f8276-153">`[Location <String>]`: Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="f8276-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f8276-154">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="f8276-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f8276-155">`[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f8276-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f8276-156">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="f8276-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f8276-157">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f8276-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f8276-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8276-158">RELATED LINKS</span></span>

