---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109558"
---
# <span data-ttu-id="150da-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="150da-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="150da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="150da-102">SYNOPSIS</span></span>
<span data-ttu-id="150da-103">Verilen bir çerçeve altındaki bir MariaDB bağlantı dizesini alın.</span><span class="sxs-lookup"><span data-stu-id="150da-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="150da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="150da-104">SYNTAX</span></span>

### <span data-ttu-id="150da-105">ServerName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="150da-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="150da-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="150da-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="150da-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="150da-107">DESCRIPTION</span></span>
<span data-ttu-id="150da-108">Verilen bir çerçeve altındaki bir MariaDB bağlantı dizesini alın.</span><span class="sxs-lookup"><span data-stu-id="150da-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="150da-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="150da-109">EXAMPLES</span></span>

### <span data-ttu-id="150da-110">Örnek 1: MariaDB bağlantı dizesini alma</span><span class="sxs-lookup"><span data-stu-id="150da-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="150da-111">Bu komut, MariaDB bağlantı dizesini alır.</span><span class="sxs-lookup"><span data-stu-id="150da-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="150da-112">Örnek 2: MariaDB bağlantı dizesini alma</span><span class="sxs-lookup"><span data-stu-id="150da-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="150da-113">Bu komut, MariaDB bağlantı dizesini alır.</span><span class="sxs-lookup"><span data-stu-id="150da-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="150da-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="150da-114">PARAMETERS</span></span>

### <span data-ttu-id="150da-115">-İstemci</span><span class="sxs-lookup"><span data-stu-id="150da-115">-Client</span></span>
<span data-ttu-id="150da-116">Bağlantı istemci türü</span><span class="sxs-lookup"><span data-stu-id="150da-116">Connect client type</span></span>

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

### <span data-ttu-id="150da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="150da-117">-DefaultProfile</span></span>
<span data-ttu-id="150da-118">bölge DefaultParameters Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="150da-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="150da-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="150da-119">-InputObject</span></span>
<span data-ttu-id="150da-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="150da-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="150da-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="150da-121">-Name</span></span>
<span data-ttu-id="150da-122">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="150da-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="150da-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="150da-123">-ResourceGroupName</span></span>
<span data-ttu-id="150da-124">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="150da-124">The name of the resource group that contains the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="150da-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="150da-125">-SubscriptionId</span></span>
<span data-ttu-id="150da-126">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır</span><span class="sxs-lookup"><span data-stu-id="150da-126">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="150da-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="150da-127">CommonParameters</span></span>
<span data-ttu-id="150da-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="150da-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="150da-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="150da-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="150da-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="150da-130">INPUTS</span></span>

### <span data-ttu-id="150da-131">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="150da-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="150da-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="150da-132">OUTPUTS</span></span>

### <span data-ttu-id="150da-133">System. String</span><span class="sxs-lookup"><span data-stu-id="150da-133">System.String</span></span>

## <span data-ttu-id="150da-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="150da-134">NOTES</span></span>

<span data-ttu-id="150da-135">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="150da-135">ALIASES</span></span>

<span data-ttu-id="150da-136">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="150da-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="150da-137">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="150da-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="150da-138">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="150da-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="150da-139">INPUTOBJECT <IServer> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="150da-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="150da-140">`Location <String>`: Kaynağın bulunduğu konum.</span><span class="sxs-lookup"><span data-stu-id="150da-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="150da-141">`[Tag <ITrackedResourceTags>]`: Anahtar-değer çiftleri biçiminde uygulamaya özgü meta veriler.</span><span class="sxs-lookup"><span data-stu-id="150da-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="150da-142">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="150da-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="150da-143">`[AdministratorLogin <String>]`: Yöneticinin sunucunun oturum açma adı.</span><span class="sxs-lookup"><span data-stu-id="150da-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="150da-144">Yalnızca sunucu oluşturulduğunda belirtilebilir (ve oluşturma için gereklidir).</span><span class="sxs-lookup"><span data-stu-id="150da-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="150da-145">`[EarliestRestoreDate <DateTime?>]`: En erken geri yükleme noktası oluşturulma zamanı (ISO8601 biçimi)</span><span class="sxs-lookup"><span data-stu-id="150da-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="150da-146">`[FullyQualifiedDomainName <String>]`: Sunucunun tam nitelikli etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="150da-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="150da-147">`[IdentityType <IdentityType?>]`: Kimlik türü.</span><span class="sxs-lookup"><span data-stu-id="150da-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="150da-148">Kaynak için bir Azure Active Directory sorumlusu oluşturmak ve atamak için bunu ' SystemAssigned ' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="150da-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="150da-149">`[MasterServerId <String>]`: Bir çoğaltma sunucusunun ana sunucu kimliği.</span><span class="sxs-lookup"><span data-stu-id="150da-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="150da-150">`[ReplicaCapacity <Int32?>]`: Ana sunucunun sahip olduğu en fazla yineleme sayısı.</span><span class="sxs-lookup"><span data-stu-id="150da-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="150da-151">`[ReplicationRole <String>]`: Sunucunun çoğaltma rolü.</span><span class="sxs-lookup"><span data-stu-id="150da-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="150da-152">`[SkuCapacity <Int32?>]`: Sunucunun COMPUTE birimlerini temsil eden ölçeklendirme/Out kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="150da-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="150da-153">`[SkuFamily <String>]`: Donanım ailesi.</span><span class="sxs-lookup"><span data-stu-id="150da-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="150da-154">`[SkuName <String>]`: SKU 'nun adı, genellikle katman + aile + çekirdek; Örneğin, B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="150da-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="150da-155">`[SkuSize <String>]`: Kaynak tarafından uygun şekilde yorumlanabilecek boyut kodu.</span><span class="sxs-lookup"><span data-stu-id="150da-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="150da-156">`[SkuTier <SkuTier?>]`: Belirli SKU 'nun katmanı, örneğin. temel.</span><span class="sxs-lookup"><span data-stu-id="150da-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="150da-157">`[SslEnforcement <SslEnforcementEnum?>]`: Sunucuya bağlanırken SSL zorlamayı etkinleştir veya yok.</span><span class="sxs-lookup"><span data-stu-id="150da-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="150da-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Sunucunun yedekleme bekletme günleri.</span><span class="sxs-lookup"><span data-stu-id="150da-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="150da-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: OneDrive 'ı etkinleştir-sunucu yedeklemesi için değil.</span><span class="sxs-lookup"><span data-stu-id="150da-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="150da-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Otomatik büyüme özelliğini etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="150da-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="150da-161">`[StorageProfileStorageMb <Int32?>]`: Sunucuda izin verilen maks depolama alanı.</span><span class="sxs-lookup"><span data-stu-id="150da-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="150da-162">`[UserVisibleState <ServerState?>]`: Kullanıcının görebileceği bir sunucunun durumu.</span><span class="sxs-lookup"><span data-stu-id="150da-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="150da-163">`[Version <ServerVersion?>]`: Sunucu sürümü.</span><span class="sxs-lookup"><span data-stu-id="150da-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="150da-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="150da-164">RELATED LINKS</span></span>

