---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 3a9fedc637f8400b952d823a98dfe0abaa1d40d3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937176"
---
# <span data-ttu-id="a3336-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3336-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="a3336-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3336-102">SYNOPSIS</span></span>
<span data-ttu-id="a3336-103">Ada göre belirli bir yedekleme konumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="a3336-103">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="a3336-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3336-104">SYNTAX</span></span>

### <span data-ttu-id="a3336-105">Get (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a3336-105">Get (Default)</span></span>
```
Get-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a3336-106">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="a3336-106">GetViaIdentity</span></span>
```
Get-AzsBackupConfiguration -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3336-107">Listeniz</span><span class="sxs-lookup"><span data-stu-id="a3336-107">List</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a3336-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3336-108">DESCRIPTION</span></span>
<span data-ttu-id="a3336-109">Ada göre belirli bir yedekleme konumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="a3336-109">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="a3336-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3336-110">EXAMPLES</span></span>

### <span data-ttu-id="a3336-111">Örnek 1: Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3336-111">Example 1: Get-AzsBackupConfiguration</span></span>
```powershell
PS C:\> Get-AzsBackupConfiguration

```

<span data-ttu-id="a3336-112">Azure yığın yedekleme yapılandırmasını edinin.</span><span class="sxs-lookup"><span data-stu-id="a3336-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="a3336-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3336-113">PARAMETERS</span></span>

### <span data-ttu-id="a3336-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3336-114">-DefaultProfile</span></span>
<span data-ttu-id="a3336-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3336-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3336-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3336-116">-InputObject</span></span>
<span data-ttu-id="a3336-117">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3336-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a3336-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="a3336-118">-Location</span></span>
<span data-ttu-id="a3336-119">Yedekleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="a3336-119">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a3336-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3336-120">-ResourceGroupName</span></span>
<span data-ttu-id="a3336-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a3336-121">Name of the resource group.</span></span>

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

### <span data-ttu-id="a3336-122">-Atla</span><span class="sxs-lookup"><span data-stu-id="a3336-122">-Skip</span></span>
<span data-ttu-id="a3336-123">OData Skip parametresi.</span><span class="sxs-lookup"><span data-stu-id="a3336-123">OData skip parameter.</span></span>

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

### <span data-ttu-id="a3336-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a3336-124">-SubscriptionId</span></span>
<span data-ttu-id="a3336-125">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="a3336-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a3336-126">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a3336-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a3336-127">-Üst</span><span class="sxs-lookup"><span data-stu-id="a3336-127">-Top</span></span>
<span data-ttu-id="a3336-128">OData üst parametresi.</span><span class="sxs-lookup"><span data-stu-id="a3336-128">OData top parameter.</span></span>

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

### <span data-ttu-id="a3336-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3336-129">CommonParameters</span></span>
<span data-ttu-id="a3336-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3336-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3336-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a3336-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3336-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3336-132">INPUTS</span></span>

### <span data-ttu-id="a3336-133">Microsoft. Azure. PowerShell. cmdlet. Yedeklemeadmin. modeller. ıbackupadminıdentity</span><span class="sxs-lookup"><span data-stu-id="a3336-133">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="a3336-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3336-134">OUTPUTS</span></span>

### <span data-ttu-id="a3336-135">Microsoft. Azure. PowerShell. cmdlet. Yedeklemeadmin. modeller. Api20180901. ıbackuplocation</span><span class="sxs-lookup"><span data-stu-id="a3336-135">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="a3336-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3336-136">NOTES</span></span>

<span data-ttu-id="a3336-137">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a3336-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a3336-138">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a3336-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a3336-139">INPUTOBJECT <IBackupAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="a3336-139">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a3336-140">`[Backup <String>]`: Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="a3336-140">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="a3336-141">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="a3336-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a3336-142">`[Location <String>]`: Yedekleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="a3336-142">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="a3336-143">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a3336-143">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="a3336-144">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="a3336-144">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a3336-145">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a3336-145">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a3336-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3336-146">RELATED LINKS</span></span>

