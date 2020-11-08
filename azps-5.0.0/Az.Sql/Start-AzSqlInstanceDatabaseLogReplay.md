---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 61a87f61efaa889af830cc7bdaa44bcf0b7fc698
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275648"
---
# <span data-ttu-id="7bd0c-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="7bd0c-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="7bd0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bd0c-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd0c-103">Verilen parametrelerle bir günlük yürütme hizmeti başlatır.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="7bd0c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7bd0c-104">SYNTAX</span></span>

### <span data-ttu-id="7bd0c-105">Logreplayınstancedatabasefrominınputparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7bd0c-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bd0c-106">Logreplayınstancedatabasefrolauressqlmanageddatabasemodelınstancedefinition</span><span class="sxs-lookup"><span data-stu-id="7bd0c-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7bd0c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7bd0c-107">DESCRIPTION</span></span>
<span data-ttu-id="7bd0c-108">**Start-Azsqlınstancedatabaselogreplay** cmdlet 'i log Replay hizmeti başlangıcını başlatır.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="7bd0c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7bd0c-109">EXAMPLES</span></span>

### <span data-ttu-id="7bd0c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7bd0c-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="7bd0c-111">Bu komut, yeni yönetilen veritabanı oluşturur ve last_backup. bak geri yüklenene kadar, verilen kapsayıcıdan yedekleri geri yüklemeye başlar.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="7bd0c-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7bd0c-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="7bd0c-113">Bu komut, yeni yönetilen veritabanı oluşturur ve Complete-AzSqlInstanceDatabaseLogReplay son yedekleme işlemi ile çağrılana kadar yedekleri verilen kapsayıcıdan geri yüklemeye başlar.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="7bd0c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7bd0c-114">PARAMETERS</span></span>

### <span data-ttu-id="7bd0c-115">-Automediatereser</span><span class="sxs-lookup"><span data-stu-id="7bd0c-115">-AutoCompleteRestore</span></span>
<span data-ttu-id="7bd0c-116">Tamamlandığında geri yükleme 'nin geri yükleme olup olmayacağını gösterge.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-116">The indicator whether or not to auto-complete restore upon completion.</span></span>

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

### <span data-ttu-id="7bd0c-117">-Harmanlama</span><span class="sxs-lookup"><span data-stu-id="7bd0c-117">-Collation</span></span>
<span data-ttu-id="7bd0c-118">Kullanılacak örnek veritabanının harmanlaması.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-118">The collation of the instance database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd0c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd0c-119">-DefaultProfile</span></span>
<span data-ttu-id="7bd0c-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd0c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bd0c-121">-InputObject</span></span>
<span data-ttu-id="7bd0c-122">Örnek veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-122">The instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd0c-123">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7bd0c-123">-InstanceName</span></span>
<span data-ttu-id="7bd0c-124">Örneğin adı.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-124">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd0c-125">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="7bd0c-125">-LastBackupName</span></span>
<span data-ttu-id="7bd0c-126">Geri yüklenecek son yedekleme dosyasının adı.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-126">The name of the last backup file to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd0c-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="7bd0c-127">-Name</span></span>
<span data-ttu-id="7bd0c-128">Örnek veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-128">The name of the instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd0c-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7bd0c-129">-PassThru</span></span>
<span data-ttu-id="7bd0c-130">Eşitleme grubunu iade edilip edilmeyeceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-130">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="7bd0c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bd0c-131">-ResourceGroupName</span></span>
<span data-ttu-id="7bd0c-132">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd0c-133">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="7bd0c-133">-StorageContainerSasToken</span></span>
<span data-ttu-id="7bd0c-134">Depolama kapsayıcısı SAS belirteci.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-134">The storage container Sas token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasToken

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd0c-135">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="7bd0c-135">-StorageContainerUri</span></span>
<span data-ttu-id="7bd0c-136">Depolama kapsayıcısı URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-136">The storage container URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Storage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd0c-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="7bd0c-137">-Confirm</span></span>
<span data-ttu-id="7bd0c-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bd0c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bd0c-139">-WhatIf</span></span>
<span data-ttu-id="7bd0c-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bd0c-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bd0c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd0c-142">CommonParameters</span></span>
<span data-ttu-id="7bd0c-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd0c-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7bd0c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd0c-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7bd0c-145">INPUTS</span></span>

### <span data-ttu-id="7bd0c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7bd0c-146">System.String</span></span>

### <span data-ttu-id="7bd0c-147">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="7bd0c-147">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="7bd0c-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7bd0c-148">OUTPUTS</span></span>

### <span data-ttu-id="7bd0c-149">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="7bd0c-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="7bd0c-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7bd0c-150">NOTES</span></span>

## <span data-ttu-id="7bd0c-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7bd0c-151">RELATED LINKS</span></span>
