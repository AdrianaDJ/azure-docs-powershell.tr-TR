---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackup
schema: 2.0.0
ms.openlocfilehash: 2c2d517da3be62ff407ca17577edefcf7322ad55
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937174"
---
# <span data-ttu-id="d499e-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="d499e-101">Get-AzsBackup</span></span>

## <span data-ttu-id="d499e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d499e-102">SYNOPSIS</span></span>
<span data-ttu-id="d499e-103">Ad temelinde bir konumdan yedekleme döndürür.</span><span class="sxs-lookup"><span data-stu-id="d499e-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="d499e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d499e-104">SYNTAX</span></span>

### <span data-ttu-id="d499e-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d499e-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d499e-106">Al</span><span class="sxs-lookup"><span data-stu-id="d499e-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d499e-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="d499e-107">GetViaIdentity</span></span>
```
Get-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d499e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d499e-108">DESCRIPTION</span></span>
<span data-ttu-id="d499e-109">Ad temelinde bir konumdan yedekleme döndürür.</span><span class="sxs-lookup"><span data-stu-id="d499e-109">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="d499e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d499e-110">EXAMPLES</span></span>

### <span data-ttu-id="d499e-111">Örnek 1: yedeklemeleri Listele</span><span class="sxs-lookup"><span data-stu-id="d499e-111">Example 1: List Backups</span></span>
```powershell
PS C:\> Get-AzsBackup

```

<span data-ttu-id="d499e-112">Tüm Azure yığın yedeklemelerini hakkında bilgi alın.</span><span class="sxs-lookup"><span data-stu-id="d499e-112">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="d499e-113">Örnek 2: belirli bir yedekleme alın</span><span class="sxs-lookup"><span data-stu-id="d499e-113">Example 2: Get specific backup</span></span>
```powershell
PS C:\> Get-AzsBackup -Name 'backupName'

```

<span data-ttu-id="d499e-114">Belirtilen Azure yığın yedeklemesi için bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="d499e-114">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="d499e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d499e-115">PARAMETERS</span></span>

### <span data-ttu-id="d499e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d499e-116">-DefaultProfile</span></span>
<span data-ttu-id="d499e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d499e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d499e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d499e-118">-InputObject</span></span>
<span data-ttu-id="d499e-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d499e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d499e-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="d499e-120">-Location</span></span>
<span data-ttu-id="d499e-121">Yedekleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="d499e-121">Name of the backup location.</span></span>

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

### <span data-ttu-id="d499e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d499e-122">-Name</span></span>
<span data-ttu-id="d499e-123">Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="d499e-123">Name of the backup.</span></span>

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

### <span data-ttu-id="d499e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d499e-124">-ResourceGroupName</span></span>
<span data-ttu-id="d499e-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d499e-125">Name of the resource group.</span></span>

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

### <span data-ttu-id="d499e-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="d499e-126">-Skip</span></span>
<span data-ttu-id="d499e-127">OData Skip parametresi.</span><span class="sxs-lookup"><span data-stu-id="d499e-127">OData skip parameter.</span></span>

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

### <span data-ttu-id="d499e-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d499e-128">-SubscriptionId</span></span>
<span data-ttu-id="d499e-129">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="d499e-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d499e-130">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d499e-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d499e-131">-Üst</span><span class="sxs-lookup"><span data-stu-id="d499e-131">-Top</span></span>
<span data-ttu-id="d499e-132">OData üst parametresi.</span><span class="sxs-lookup"><span data-stu-id="d499e-132">OData top parameter.</span></span>

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

### <span data-ttu-id="d499e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d499e-133">CommonParameters</span></span>
<span data-ttu-id="d499e-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d499e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d499e-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d499e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d499e-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d499e-136">INPUTS</span></span>

### <span data-ttu-id="d499e-137">Microsoft. Azure. PowerShell. cmdlet. Yedeklemeadmin. modeller. ıbackupadminıdentity</span><span class="sxs-lookup"><span data-stu-id="d499e-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="d499e-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d499e-138">OUTPUTS</span></span>

### <span data-ttu-id="d499e-139">Microsoft. Azure. PowerShell. cmdlet. Yedeklemeadmin. modeller. Api20180901. IBackup</span><span class="sxs-lookup"><span data-stu-id="d499e-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="d499e-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d499e-140">NOTES</span></span>

<span data-ttu-id="d499e-141">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d499e-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d499e-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d499e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d499e-143">INPUTOBJECT <IBackupAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="d499e-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d499e-144">`[Backup <String>]`: Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="d499e-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="d499e-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="d499e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d499e-146">`[Location <String>]`: Yedekleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="d499e-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="d499e-147">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d499e-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="d499e-148">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="d499e-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d499e-149">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d499e-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d499e-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d499e-150">RELATED LINKS</span></span>

