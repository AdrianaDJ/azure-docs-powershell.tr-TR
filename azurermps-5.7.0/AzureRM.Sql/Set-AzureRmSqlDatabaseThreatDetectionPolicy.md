---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: aa70b94614f8a0826a5d1563439afa8cb9ef6d95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593362"
---
# <span data-ttu-id="e6ab8-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e6ab8-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="e6ab8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ab8-103">Veritabanında tehdit algılama ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-103">Sets a threat detection policy on a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6ab8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6ab8-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6ab8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6ab8-105">DESCRIPTION</span></span>
<span data-ttu-id="e6ab8-106">**Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet 'ı BIR Azure SQL veritabanında tehdit algılama ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-106">The **Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="e6ab8-107">Veritabanında tehdit algılamasını etkinleştirmek için bu veritabanında denetim ilkesi etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>

<span data-ttu-id="e6ab8-108">Bu cmdlet 'i kullanmak için, veritabanını tanımlayacak *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="e6ab8-109">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e6ab8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6ab8-110">EXAMPLES</span></span>

### <span data-ttu-id="e6ab8-111">Örnek 1: veritabanı için tehdit algılama ilkesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="e6ab8-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="e6ab8-112">Bu komut, server01 adındaki sunucuda Database01 adlı bir veritabanı için tehdit algılama ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="e6ab8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6ab8-113">PARAMETERS</span></span>

### <span data-ttu-id="e6ab8-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e6ab8-114">-DatabaseName</span></span>
<span data-ttu-id="e6ab8-115">İlkenin ayarlandığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-115">Specifies the name of the database where the policy is set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ab8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ab8-116">-DefaultProfile</span></span>
<span data-ttu-id="e6ab8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e6ab8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ab8-118">-Eda</span><span class="sxs-lookup"><span data-stu-id="e6ab8-118">-EmailAdmins</span></span>
<span data-ttu-id="e6ab8-119">Tehdit algılama ilkesinin e-posta kullanarak yöneticilere mı ait olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-119">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ab8-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="e6ab8-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="e6ab8-121">İlkeden dışlanacak algılama türleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-121">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="e6ab8-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e6ab8-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6ab8-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="e6ab8-123">Sql_Injection</span></span> 
- <span data-ttu-id="e6ab8-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="e6ab8-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="e6ab8-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="e6ab8-125">Access_Anomaly</span></span> 
- <span data-ttu-id="e6ab8-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e6ab8-126">None</span></span>

```yaml
Type: DetectionType[]
Parameter Sets: (All)
Aliases:
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ab8-127">-Notificationrecipientşeması ILS</span><span class="sxs-lookup"><span data-stu-id="e6ab8-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="e6ab8-128">İlkenin uyarıları gönderdiği e-posta adreslerinin noktalı virgülle ayrılmış listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-128">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ab8-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e6ab8-129">-PassThru</span></span>
<span data-ttu-id="e6ab8-130">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e6ab8-131">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e6ab8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6ab8-132">-ResourceGroupName</span></span>
<span data-ttu-id="e6ab8-133">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-133">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ab8-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e6ab8-134">-RetentionInDays</span></span>
<span data-ttu-id="e6ab8-135">Denetim günlükleri için bekletme günü sayısı</span><span class="sxs-lookup"><span data-stu-id="e6ab8-135">The number of retention days for the audit logs</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ab8-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e6ab8-136">-ServerName</span></span>
<span data-ttu-id="e6ab8-137">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-137">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ab8-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e6ab8-138">-StorageAccountName</span></span>
<span data-ttu-id="e6ab8-139">Kullanılacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="e6ab8-140">Joker karakterlere izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-140">Wildcards are not permitted.</span></span> <span data-ttu-id="e6ab8-141">Bu parametre gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-141">This parameter is not required.</span></span> <span data-ttu-id="e6ab8-142">Bu parametre sağlanmadıysa cmdlet, veritabanının tehdit algılama ilkesinin bir parçası olarak daha önce tanımlanan depolama hesabını kullanır.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="e6ab8-143">Bir veritabanı tehdit algılama ilkesi ilk kez tanımlandıysa ve bu parametre sağlanmadıysa cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-143">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ab8-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="e6ab8-144">-Confirm</span></span>
<span data-ttu-id="e6ab8-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ab8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6ab8-146">-WhatIf</span></span>
<span data-ttu-id="e6ab8-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6ab8-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ab8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ab8-149">CommonParameters</span></span>
<span data-ttu-id="e6ab8-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ab8-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6ab8-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ab8-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6ab8-152">INPUTS</span></span>

###  
<span data-ttu-id="e6ab8-153">Bu cmdlet 'e giriş kanalı oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-153">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="e6ab8-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6ab8-154">OUTPUTS</span></span>

### <span data-ttu-id="e6ab8-155">Microsoft. Azure. Commands. Sql. ThreatDetection. model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e6ab8-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="e6ab8-156">Bu cmdlet, bir **model. DatabaseThreatDetectionPolicyModel** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="e6ab8-156">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="e6ab8-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6ab8-157">NOTES</span></span>

## <span data-ttu-id="e6ab8-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6ab8-158">RELATED LINKS</span></span>

[<span data-ttu-id="e6ab8-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e6ab8-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="e6ab8-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e6ab8-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="e6ab8-161">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="e6ab8-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


