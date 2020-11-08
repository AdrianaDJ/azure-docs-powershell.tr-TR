---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 3b9ca8c4aa236b690bbe0dfe09c35f0ebc8a5b22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108174"
---
# <span data-ttu-id="c7edf-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="c7edf-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="c7edf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7edf-102">SYNOPSIS</span></span>
<span data-ttu-id="c7edf-103">Yeni sunucu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c7edf-103">Creates a new server.</span></span>

## <span data-ttu-id="c7edf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7edf-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c7edf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7edf-105">DESCRIPTION</span></span>
<span data-ttu-id="c7edf-106">Yeni sunucu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c7edf-106">Creates a new server.</span></span>

## <span data-ttu-id="c7edf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7edf-107">EXAMPLES</span></span>

### <span data-ttu-id="c7edf-108">Örnek 1: yeni bir MySql sunucusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="c7edf-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c7edf-109">Bu cmdlet 'ler yeni bir MySql sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c7edf-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="c7edf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7edf-110">PARAMETERS</span></span>

### <span data-ttu-id="c7edf-111">-\Administrators</span><span class="sxs-lookup"><span data-stu-id="c7edf-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="c7edf-112">Kaynağın bulunduğu konum.</span><span class="sxs-lookup"><span data-stu-id="c7edf-112">The location the resource resides in.</span></span>

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

### <span data-ttu-id="c7edf-113">-\Administrators Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="c7edf-113">-AdministratorUserName</span></span>
<span data-ttu-id="c7edf-114">Kaynağın bulunduğu konum.</span><span class="sxs-lookup"><span data-stu-id="c7edf-114">The location the resource resides in.</span></span>

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

### <span data-ttu-id="c7edf-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="c7edf-115">-AsJob</span></span>
<span data-ttu-id="c7edf-116">Komutu iş olarak çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="c7edf-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="c7edf-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="c7edf-117">-BackupRetentionDay</span></span>
<span data-ttu-id="c7edf-118">Sunucu için yedekleme bekletme günleri.</span><span class="sxs-lookup"><span data-stu-id="c7edf-118">Backup retention days for the server.</span></span>
<span data-ttu-id="c7edf-119">Gün sayısı 7 ile 35 arasındadır.</span><span class="sxs-lookup"><span data-stu-id="c7edf-119">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="c7edf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7edf-120">-DefaultProfile</span></span>
<span data-ttu-id="c7edf-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c7edf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7edf-122">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="c7edf-122">-GeoRedundantBackup</span></span>
<span data-ttu-id="c7edf-123">Coğrafi olarak yedekli veya sunucu yedeklemesi için değil özelliğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="c7edf-123">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7edf-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="c7edf-124">-Location</span></span>
<span data-ttu-id="c7edf-125">Kaynağın bulunduğu konum.</span><span class="sxs-lookup"><span data-stu-id="c7edf-125">The location the resource resides in.</span></span>

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

### <span data-ttu-id="c7edf-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="c7edf-126">-Name</span></span>
<span data-ttu-id="c7edf-127">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="c7edf-127">The name of the server.</span></span>

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

### <span data-ttu-id="c7edf-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c7edf-128">-NoWait</span></span>
<span data-ttu-id="c7edf-129">Komutu zaman uyumsuz olarak çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="c7edf-129">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="c7edf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7edf-130">-ResourceGroupName</span></span>
<span data-ttu-id="c7edf-131">Kaynağı içeren kaynak grubunun adı, bu değeri Azure Kaynak Yöneticisi API 'sinden veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7edf-131">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c7edf-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="c7edf-132">-Sku</span></span>
<span data-ttu-id="c7edf-133">SKU 'nun adı, genellikle katman + aile + çekirdek; Örneğin, B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="c7edf-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="c7edf-134">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="c7edf-134">-SslEnforcement</span></span>
<span data-ttu-id="c7edf-135">SSL zorlamayı etkinleştirme veya sunucuya bağlanırken kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="c7edf-135">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7edf-136">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="c7edf-136">-StorageAutogrow</span></span>
<span data-ttu-id="c7edf-137">Otomatik büyüme özelliğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="c7edf-137">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7edf-138">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="c7edf-138">-StorageInMb</span></span>
<span data-ttu-id="c7edf-139">Sunucuda izin verilen maks depolama alanı.</span><span class="sxs-lookup"><span data-stu-id="c7edf-139">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="c7edf-140">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c7edf-140">-SubscriptionId</span></span>
<span data-ttu-id="c7edf-141">Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c7edf-141">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="c7edf-142">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c7edf-142">-Tag</span></span>
<span data-ttu-id="c7edf-143">Anahtar-değer çiftleri biçiminde uygulamaya özgü meta veriler.</span><span class="sxs-lookup"><span data-stu-id="c7edf-143">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="c7edf-144">-Version</span><span class="sxs-lookup"><span data-stu-id="c7edf-144">-Version</span></span>
<span data-ttu-id="c7edf-145">Sunucu sürümü.</span><span class="sxs-lookup"><span data-stu-id="c7edf-145">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7edf-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="c7edf-146">-Confirm</span></span>
<span data-ttu-id="c7edf-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c7edf-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7edf-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7edf-148">-WhatIf</span></span>
<span data-ttu-id="c7edf-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7edf-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7edf-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c7edf-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7edf-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7edf-151">CommonParameters</span></span>
<span data-ttu-id="c7edf-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7edf-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7edf-153">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c7edf-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7edf-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7edf-154">INPUTS</span></span>

## <span data-ttu-id="c7edf-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7edf-155">OUTPUTS</span></span>

### <span data-ttu-id="c7edf-156">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="c7edf-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="c7edf-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7edf-157">NOTES</span></span>

<span data-ttu-id="c7edf-158">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c7edf-158">ALIASES</span></span>

## <span data-ttu-id="c7edf-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7edf-159">RELATED LINKS</span></span>

