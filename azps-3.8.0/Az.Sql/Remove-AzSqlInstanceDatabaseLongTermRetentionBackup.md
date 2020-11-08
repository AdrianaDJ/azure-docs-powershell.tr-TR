---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: c52b0a9cafbb5a3e61af3a044ef834e499e88bc5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098288"
---
# <span data-ttu-id="5268f-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="5268f-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="5268f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5268f-102">SYNOPSIS</span></span>
<span data-ttu-id="5268f-103">Uzun süreli bekletme yedeklemesi siler.</span><span class="sxs-lookup"><span data-stu-id="5268f-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="5268f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5268f-104">SYNTAX</span></span>

### <span data-ttu-id="5268f-105">RemoveBackupDefault (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5268f-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5268f-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="5268f-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5268f-107">Removebackupbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="5268f-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5268f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5268f-108">DESCRIPTION</span></span>
<span data-ttu-id="5268f-109">**Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet 'i belirtilen yedeği siler.</span><span class="sxs-lookup"><span data-stu-id="5268f-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="5268f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5268f-110">EXAMPLES</span></span>

### <span data-ttu-id="5268f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5268f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="5268f-112">Adı ile birlikte silme: 15 be823c-7E/c-49vseç8-819f-a3fdcavseç92215; 132268250550000000</span><span class="sxs-lookup"><span data-stu-id="5268f-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="5268f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5268f-113">PARAMETERS</span></span>

### <span data-ttu-id="5268f-114">-BackupName</span><span class="sxs-lookup"><span data-stu-id="5268f-114">-BackupName</span></span>
<span data-ttu-id="5268f-115">Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="5268f-115">The name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5268f-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5268f-116">-DatabaseName</span></span>
<span data-ttu-id="5268f-117">Yedeğin kimden olduğu yönetilen veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="5268f-117">The name of the Managed Database the backup is from.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5268f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5268f-118">-DefaultProfile</span></span>
<span data-ttu-id="5268f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5268f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5268f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5268f-120">-Force</span></span>
<span data-ttu-id="5268f-121">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="5268f-121">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5268f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5268f-122">-InputObject</span></span>
<span data-ttu-id="5268f-123">Kaldırılacak veritabanı uzun süreli bekletme yedekleme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5268f-123">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: AzureSqlManagedDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5268f-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="5268f-124">-InstanceName</span></span>
<span data-ttu-id="5268f-125">Yedeğin altında bulunduğu yönetilen örneğin adı.</span><span class="sxs-lookup"><span data-stu-id="5268f-125">The name of the Managed Instance the backup is under.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5268f-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="5268f-126">-Location</span></span>
<span data-ttu-id="5268f-127">Yedeklemelerin kaynak yönetimli örneğinin konumu.</span><span class="sxs-lookup"><span data-stu-id="5268f-127">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5268f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5268f-128">-ResourceGroupName</span></span>
<span data-ttu-id="5268f-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5268f-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5268f-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5268f-130">-ResourceId</span></span>
<span data-ttu-id="5268f-131">Kaldırılacak veritabanı uzun süreli bekletme yedeklemesinin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5268f-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5268f-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="5268f-132">-Confirm</span></span>
<span data-ttu-id="5268f-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5268f-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5268f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5268f-134">-WhatIf</span></span>
<span data-ttu-id="5268f-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5268f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5268f-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5268f-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5268f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5268f-137">CommonParameters</span></span>
<span data-ttu-id="5268f-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5268f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5268f-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5268f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5268f-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5268f-140">INPUTS</span></span>

### <span data-ttu-id="5268f-141">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="5268f-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="5268f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5268f-142">System.String</span></span>

## <span data-ttu-id="5268f-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5268f-143">OUTPUTS</span></span>

### <span data-ttu-id="5268f-144">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="5268f-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="5268f-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5268f-145">NOTES</span></span>

## <span data-ttu-id="5268f-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5268f-146">RELATED LINKS</span></span>

[<span data-ttu-id="5268f-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="5268f-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="5268f-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5268f-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="5268f-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5268f-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="5268f-150">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="5268f-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)