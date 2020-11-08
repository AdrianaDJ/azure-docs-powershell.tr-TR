---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 3a9fedc637f8400b952d823a98dfe0abaa1d40d3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105354"
---
# <span data-ttu-id="a2a12-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2a12-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="a2a12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2a12-102">SYNOPSIS</span></span>
<span data-ttu-id="a2a12-103">Ada göre belirli bir yedekleme konumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="a2a12-103">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="a2a12-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2a12-104">SYNTAX</span></span>

### <span data-ttu-id="a2a12-105">Get (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a2a12-105">Get (Default)</span></span>
```
Get-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a2a12-106">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="a2a12-106">GetViaIdentity</span></span>
```
Get-AzsBackupConfiguration -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2a12-107">Listeniz</span><span class="sxs-lookup"><span data-stu-id="a2a12-107">List</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a2a12-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2a12-108">DESCRIPTION</span></span>
<span data-ttu-id="a2a12-109">Ada göre belirli bir yedekleme konumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="a2a12-109">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="a2a12-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2a12-110">EXAMPLES</span></span>

### <span data-ttu-id="a2a12-111">Örnek 1: Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2a12-111">Example 1: Get-AzsBackupConfiguration</span></span>
```powershell
PS C:\> Get-AzsBackupConfiguration

```

<span data-ttu-id="a2a12-112">Azure yığın yedekleme yapılandırmasını edinin.</span><span class="sxs-lookup"><span data-stu-id="a2a12-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="a2a12-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2a12-113">PARAMETERS</span></span>

### <span data-ttu-id="a2a12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2a12-114">-DefaultProfile</span></span>
<span data-ttu-id="a2a12-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a2a12-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2a12-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2a12-116">-InputObject</span></span>
<span data-ttu-id="a2a12-117">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a2a12-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a2a12-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="a2a12-118">-Location</span></span>
<span data-ttu-id="a2a12-119">Yedekleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="a2a12-119">Name of the backup location.</span></span>

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

### <span data-ttu-id="a2a12-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2a12-120">-ResourceGroupName</span></span>
<span data-ttu-id="a2a12-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a2a12-121">Name of the resource group.</span></span>

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

### <span data-ttu-id="a2a12-122">-Atla</span><span class="sxs-lookup"><span data-stu-id="a2a12-122">-Skip</span></span>
<span data-ttu-id="a2a12-123">OData Skip parametresi.</span><span class="sxs-lookup"><span data-stu-id="a2a12-123">OData skip parameter.</span></span>

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

### <span data-ttu-id="a2a12-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a2a12-124">-SubscriptionId</span></span>
<span data-ttu-id="a2a12-125">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="a2a12-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a2a12-126">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a2a12-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a2a12-127">-Üst</span><span class="sxs-lookup"><span data-stu-id="a2a12-127">-Top</span></span>
<span data-ttu-id="a2a12-128">OData üst parametresi.</span><span class="sxs-lookup"><span data-stu-id="a2a12-128">OData top parameter.</span></span>

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

### <span data-ttu-id="a2a12-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2a12-129">CommonParameters</span></span>
<span data-ttu-id="a2a12-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2a12-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2a12-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a2a12-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2a12-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2a12-132">INPUTS</span></span>

### <span data-ttu-id="a2a12-133">Microsoft. Azure. PowerShell. cmdlet. Yedeklemeadmin. modeller. ıbackupadminıdentity</span><span class="sxs-lookup"><span data-stu-id="a2a12-133">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="a2a12-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2a12-134">OUTPUTS</span></span>

### <span data-ttu-id="a2a12-135">Microsoft. Azure. PowerShell. cmdlet. Yedeklemeadmin. modeller. Api20180901. ıbackuplocation</span><span class="sxs-lookup"><span data-stu-id="a2a12-135">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="a2a12-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2a12-136">NOTES</span></span>

<span data-ttu-id="a2a12-137">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a2a12-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a2a12-138">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a2a12-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a2a12-139">INPUTOBJECT <IBackupAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="a2a12-139">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a2a12-140">`[Backup <String>]`: Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="a2a12-140">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="a2a12-141">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="a2a12-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a2a12-142">`[Location <String>]`: Yedekleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="a2a12-142">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="a2a12-143">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a2a12-143">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="a2a12-144">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="a2a12-144">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a2a12-145">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a2a12-145">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a2a12-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2a12-146">RELATED LINKS</span></span>

