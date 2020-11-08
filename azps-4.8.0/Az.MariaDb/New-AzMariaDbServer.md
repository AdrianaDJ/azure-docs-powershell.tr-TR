---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
ms.openlocfilehash: e6416fd67091fc86a5fe9844d3b1d366aaa6cb58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108190"
---
# <span data-ttu-id="f7e94-101">New-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="f7e94-101">New-AzMariaDbServer</span></span>

## <span data-ttu-id="f7e94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7e94-102">SYNOPSIS</span></span>
<span data-ttu-id="f7e94-103">Yeni bir MariaDB oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f7e94-103">Creates a new MariaDB.</span></span>

## <span data-ttu-id="f7e94-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7e94-104">SYNTAX</span></span>

```
New-AzMariaDbServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUsername <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f7e94-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7e94-105">DESCRIPTION</span></span>
<span data-ttu-id="f7e94-106">Yeni bir MariaDB oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f7e94-106">Creates a new MariaDB.</span></span>

## <span data-ttu-id="f7e94-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7e94-107">EXAMPLES</span></span>

### <span data-ttu-id="f7e94-108">Örnek 1: yeni bir Mari</span><span class="sxs-lookup"><span data-stu-id="f7e94-108">Example 1: Create a new MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbServer -Name mariadb-aassd-01 -ResourceGroupName lucas-manual-test -Sku 'B_Gen5_1' -Location eastus
cmdlet New-AzMariaDbServer at command pipeline position 1
Supply values for the following parameters:
AdministratorUsername: adminuser
AdministratorLoginPassword: ************

Name             Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----             -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-aassd-01 eastus   adminuser          10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="f7e94-109">Bu komut yeni bir MariaDB oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f7e94-109">This command creates a new MariaDB.</span></span>

## <span data-ttu-id="f7e94-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7e94-110">PARAMETERS</span></span>

### <span data-ttu-id="f7e94-111">-\Administrators</span><span class="sxs-lookup"><span data-stu-id="f7e94-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="f7e94-112">Yöneticinin parolası SecureString olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f7e94-112">Password of administrator, should be SecureString.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e94-113">-\Administrators Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="f7e94-113">-AdministratorUsername</span></span>
<span data-ttu-id="f7e94-114">Yöneticinin Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="f7e94-114">Username of administrator.</span></span>

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

### <span data-ttu-id="f7e94-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="f7e94-115">-AsJob</span></span>
<span data-ttu-id="f7e94-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="f7e94-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f7e94-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="f7e94-117">-BackupRetentionDay</span></span>
<span data-ttu-id="f7e94-118">Sunucu için yedekleme bekletme günleri.</span><span class="sxs-lookup"><span data-stu-id="f7e94-118">Backup retention days for the server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e94-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7e94-119">-DefaultProfile</span></span>
<span data-ttu-id="f7e94-120">bölge DefaultParameters Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f7e94-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7e94-121">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="f7e94-121">-GeoRedundantBackup</span></span>
<span data-ttu-id="f7e94-122">Coğrafi olarak yedekli veya sunucu yedeklemesi için değil özelliğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="f7e94-122">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e94-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="f7e94-123">-Location</span></span>
<span data-ttu-id="f7e94-124">Kaynağın bulunduğu konum.</span><span class="sxs-lookup"><span data-stu-id="f7e94-124">The location the resource resides in.</span></span>

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

### <span data-ttu-id="f7e94-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="f7e94-125">-Name</span></span>
<span data-ttu-id="f7e94-126">MariaDB sunucu adı.</span><span class="sxs-lookup"><span data-stu-id="f7e94-126">MariaDB server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e94-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f7e94-127">-NoWait</span></span>
<span data-ttu-id="f7e94-128">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="f7e94-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f7e94-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7e94-129">-ResourceGroupName</span></span>
<span data-ttu-id="f7e94-130">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f7e94-130">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="f7e94-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="f7e94-131">-Sku</span></span>
<span data-ttu-id="f7e94-132">SKU 'nun adı, genellikle katman + aile + çekirdek; Örneğin, B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="f7e94-132">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="f7e94-133">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="f7e94-133">-SslEnforcement</span></span>
<span data-ttu-id="f7e94-134">SSL zorlamayı etkinleştirme veya sunucuya bağlanırken kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="f7e94-134">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e94-135">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="f7e94-135">-StorageAutogrow</span></span>
<span data-ttu-id="f7e94-136">Otomatik büyüme özelliğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="f7e94-136">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e94-137">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="f7e94-137">-StorageInMb</span></span>
<span data-ttu-id="f7e94-138">Sunucuda izin verilen maks depolama alanı.</span><span class="sxs-lookup"><span data-stu-id="f7e94-138">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e94-139">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f7e94-139">-SubscriptionId</span></span>
<span data-ttu-id="f7e94-140">Abonelik KIMLIĞI her hizmet çağrısının URI 'sinin bir parçasıdır</span><span class="sxs-lookup"><span data-stu-id="f7e94-140">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="f7e94-141">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f7e94-141">-Tag</span></span>
<span data-ttu-id="f7e94-142">Anahtar-değer çiftleri biçiminde uygulamaya özgü meta veriler.</span><span class="sxs-lookup"><span data-stu-id="f7e94-142">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="f7e94-143">-Version</span><span class="sxs-lookup"><span data-stu-id="f7e94-143">-Version</span></span>
<span data-ttu-id="f7e94-144">Sunucu sürümü.</span><span class="sxs-lookup"><span data-stu-id="f7e94-144">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e94-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="f7e94-145">-Confirm</span></span>
<span data-ttu-id="f7e94-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f7e94-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7e94-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7e94-147">-WhatIf</span></span>
<span data-ttu-id="f7e94-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7e94-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7e94-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f7e94-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7e94-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7e94-150">CommonParameters</span></span>
<span data-ttu-id="f7e94-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7e94-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7e94-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f7e94-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7e94-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7e94-153">INPUTS</span></span>

## <span data-ttu-id="f7e94-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7e94-154">OUTPUTS</span></span>

### <span data-ttu-id="f7e94-155">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="f7e94-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="f7e94-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7e94-156">NOTES</span></span>

<span data-ttu-id="f7e94-157">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="f7e94-157">ALIASES</span></span>

## <span data-ttu-id="f7e94-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7e94-158">RELATED LINKS</span></span>

