---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackup
schema: 2.0.0
ms.openlocfilehash: 2c2d517da3be62ff407ca17577edefcf7322ad55
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105355"
---
# <span data-ttu-id="f9d37-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="f9d37-101">Get-AzsBackup</span></span>

## <span data-ttu-id="f9d37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9d37-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d37-103">Ad temelinde bir konumdan yedekleme döndürür.</span><span class="sxs-lookup"><span data-stu-id="f9d37-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="f9d37-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9d37-104">SYNTAX</span></span>

### <span data-ttu-id="f9d37-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f9d37-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f9d37-106">Al</span><span class="sxs-lookup"><span data-stu-id="f9d37-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f9d37-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="f9d37-107">GetViaIdentity</span></span>
```
Get-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f9d37-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9d37-108">DESCRIPTION</span></span>
<span data-ttu-id="f9d37-109">Ad temelinde bir konumdan yedekleme döndürür.</span><span class="sxs-lookup"><span data-stu-id="f9d37-109">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="f9d37-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9d37-110">EXAMPLES</span></span>

### <span data-ttu-id="f9d37-111">Örnek 1: yedeklemeleri Listele</span><span class="sxs-lookup"><span data-stu-id="f9d37-111">Example 1: List Backups</span></span>
```powershell
PS C:\> Get-AzsBackup

```

<span data-ttu-id="f9d37-112">Tüm Azure yığın yedeklemelerini hakkında bilgi alın.</span><span class="sxs-lookup"><span data-stu-id="f9d37-112">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="f9d37-113">Örnek 2: belirli bir yedekleme alın</span><span class="sxs-lookup"><span data-stu-id="f9d37-113">Example 2: Get specific backup</span></span>
```powershell
PS C:\> Get-AzsBackup -Name 'backupName'

```

<span data-ttu-id="f9d37-114">Belirtilen Azure yığın yedeklemesi için bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="f9d37-114">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="f9d37-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9d37-115">PARAMETERS</span></span>

### <span data-ttu-id="f9d37-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9d37-116">-DefaultProfile</span></span>
<span data-ttu-id="f9d37-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f9d37-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9d37-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9d37-118">-InputObject</span></span>
<span data-ttu-id="f9d37-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f9d37-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f9d37-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="f9d37-120">-Location</span></span>
<span data-ttu-id="f9d37-121">Yedekleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="f9d37-121">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f9d37-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f9d37-122">-Name</span></span>
<span data-ttu-id="f9d37-123">Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="f9d37-123">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f9d37-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9d37-124">-ResourceGroupName</span></span>
<span data-ttu-id="f9d37-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f9d37-125">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f9d37-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="f9d37-126">-Skip</span></span>
<span data-ttu-id="f9d37-127">OData Skip parametresi.</span><span class="sxs-lookup"><span data-stu-id="f9d37-127">OData skip parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f9d37-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f9d37-128">-SubscriptionId</span></span>
<span data-ttu-id="f9d37-129">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="f9d37-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f9d37-130">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f9d37-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f9d37-131">-Üst</span><span class="sxs-lookup"><span data-stu-id="f9d37-131">-Top</span></span>
<span data-ttu-id="f9d37-132">OData üst parametresi.</span><span class="sxs-lookup"><span data-stu-id="f9d37-132">OData top parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f9d37-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9d37-133">CommonParameters</span></span>
<span data-ttu-id="f9d37-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9d37-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9d37-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f9d37-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9d37-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9d37-136">INPUTS</span></span>

### <span data-ttu-id="f9d37-137">Microsoft. Azure. PowerShell. cmdlet. Yedeklemeadmin. modeller. ıbackupadminıdentity</span><span class="sxs-lookup"><span data-stu-id="f9d37-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="f9d37-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9d37-138">OUTPUTS</span></span>

### <span data-ttu-id="f9d37-139">Microsoft. Azure. PowerShell. cmdlet. Yedeklemeadmin. modeller. Api20180901. IBackup</span><span class="sxs-lookup"><span data-stu-id="f9d37-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="f9d37-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9d37-140">NOTES</span></span>

<span data-ttu-id="f9d37-141">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f9d37-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f9d37-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f9d37-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f9d37-143">INPUTOBJECT <IBackupAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="f9d37-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f9d37-144">`[Backup <String>]`: Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="f9d37-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="f9d37-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="f9d37-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f9d37-146">`[Location <String>]`: Yedekleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="f9d37-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="f9d37-147">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f9d37-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f9d37-148">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="f9d37-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f9d37-149">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f9d37-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f9d37-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9d37-150">RELATED LINKS</span></span>

