---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/start-azsbackup
schema: 2.0.0
ms.openlocfilehash: 37fc3ddb1c878bc8b6b1e14d920a5747edce0cd3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107034"
---
# <span data-ttu-id="3b1b0-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="3b1b0-101">Start-AzsBackup</span></span>

## <span data-ttu-id="3b1b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b1b0-102">SYNOPSIS</span></span>
<span data-ttu-id="3b1b0-103">Belirli bir konumu yedekleyin.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-103">Back up a specific location.</span></span>

## <span data-ttu-id="3b1b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b1b0-104">SYNTAX</span></span>

### <span data-ttu-id="3b1b0-105">Oluştur (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3b1b0-105">Create (Default)</span></span>
```
Start-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3b1b0-106">Createviaıdentity</span><span class="sxs-lookup"><span data-stu-id="3b1b0-106">CreateViaIdentity</span></span>
```
Start-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3b1b0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b1b0-107">DESCRIPTION</span></span>
<span data-ttu-id="3b1b0-108">Belirli bir konumu yedekleyin.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-108">Back up a specific location.</span></span>

## <span data-ttu-id="3b1b0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b1b0-109">EXAMPLES</span></span>

### <span data-ttu-id="3b1b0-110">Örnek 1: azurestack Backup 'ı başlatma</span><span class="sxs-lookup"><span data-stu-id="3b1b0-110">Example 1: Start azurestack backup</span></span>
```powershell
PS C:\>Start-AzsBackup

```

<span data-ttu-id="3b1b0-111">Azure yığın yedeklemesini başlatma.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="3b1b0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b1b0-112">PARAMETERS</span></span>

### <span data-ttu-id="3b1b0-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="3b1b0-113">-AsJob</span></span>
<span data-ttu-id="3b1b0-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="3b1b0-114">Run the command as a job</span></span>

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

### <span data-ttu-id="3b1b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b1b0-115">-DefaultProfile</span></span>
<span data-ttu-id="3b1b0-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b1b0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b1b0-117">-InputObject</span></span>
<span data-ttu-id="3b1b0-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3b1b0-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="3b1b0-119">-Location</span></span>
<span data-ttu-id="3b1b0-120">Yedekleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-120">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3b1b0-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3b1b0-121">-NoWait</span></span>
<span data-ttu-id="3b1b0-122">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="3b1b0-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3b1b0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b1b0-123">-ResourceGroupName</span></span>
<span data-ttu-id="3b1b0-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3b1b0-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="3b1b0-125">-SubscriptionId</span></span>
<span data-ttu-id="3b1b0-126">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3b1b0-127">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3b1b0-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="3b1b0-128">-Confirm</span></span>
<span data-ttu-id="3b1b0-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b1b0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b1b0-130">-WhatIf</span></span>
<span data-ttu-id="3b1b0-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b1b0-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b1b0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b1b0-133">CommonParameters</span></span>
<span data-ttu-id="3b1b0-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b1b0-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b1b0-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b1b0-136">INPUTS</span></span>

### <span data-ttu-id="3b1b0-137">Microsoft. Azure. PowerShell. cmdlet. Yedeklemeadmin. modeller. ıbackupadminıdentity</span><span class="sxs-lookup"><span data-stu-id="3b1b0-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="3b1b0-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b1b0-138">OUTPUTS</span></span>

### <span data-ttu-id="3b1b0-139">Microsoft. Azure. PowerShell. cmdlet. Yedeklemeadmin. modeller. Api20180901. IBackup</span><span class="sxs-lookup"><span data-stu-id="3b1b0-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="3b1b0-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b1b0-140">NOTES</span></span>

<span data-ttu-id="3b1b0-141">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3b1b0-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3b1b0-143">INPUTOBJECT <IBackupAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="3b1b0-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3b1b0-144">`[Backup <String>]`: Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="3b1b0-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="3b1b0-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3b1b0-146">`[Location <String>]`: Yedekleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="3b1b0-147">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="3b1b0-148">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3b1b0-149">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3b1b0-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3b1b0-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b1b0-150">RELATED LINKS</span></span>

