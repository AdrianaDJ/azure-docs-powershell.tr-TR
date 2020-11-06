---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 746a9a9908865047d5b904b5b47b71ca9c30fbd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589032"
---
# <span data-ttu-id="1107b-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1107b-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="1107b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1107b-102">SYNOPSIS</span></span>
<span data-ttu-id="1107b-103">Veritabanında tehdit algılama ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1107b-103">Sets a threat detection policy on a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1107b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1107b-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1107b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1107b-105">DESCRIPTION</span></span>
<span data-ttu-id="1107b-106">**Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet 'ı BIR Azure SQL veritabanında tehdit algılama ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1107b-106">The **Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="1107b-107">Veritabanında tehdit algılamasını etkinleştirmek için bu veritabanında denetim ilkesi etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="1107b-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>

<span data-ttu-id="1107b-108">Bu cmdlet 'i kullanmak için, veritabanını tanımlayacak *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="1107b-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="1107b-109">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="1107b-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1107b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1107b-110">EXAMPLES</span></span>

### <span data-ttu-id="1107b-111">Örnek 1: veritabanı için tehdit algılama ilkesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="1107b-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="1107b-112">Bu komut, server01 adındaki sunucuda Database01 adlı bir veritabanı için tehdit algılama ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1107b-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="1107b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1107b-113">PARAMETERS</span></span>

### <span data-ttu-id="1107b-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1107b-114">-DatabaseName</span></span>
<span data-ttu-id="1107b-115">İlkenin ayarlandığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1107b-115">Specifies the name of the database where the policy is set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1107b-116">-Eda</span><span class="sxs-lookup"><span data-stu-id="1107b-116">-EmailAdmins</span></span>
<span data-ttu-id="1107b-117">Tehdit algılama ilkesinin e-posta kullanarak yöneticilere mı ait olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1107b-117">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1107b-118">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="1107b-118">-ExcludedDetectionType</span></span>
<span data-ttu-id="1107b-119">İlkeden dışlanacak algılama türleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1107b-119">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="1107b-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1107b-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1107b-121">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="1107b-121">Sql_Injection</span></span> 
- <span data-ttu-id="1107b-122">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="1107b-122">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="1107b-123">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="1107b-123">Access_Anomaly</span></span> 
- <span data-ttu-id="1107b-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1107b-124">None</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]
Parameter Sets: (All)
Aliases: 
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1107b-125">-Notificationrecipientşeması ILS</span><span class="sxs-lookup"><span data-stu-id="1107b-125">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="1107b-126">İlkenin uyarıları gönderdiği e-posta adreslerinin noktalı virgülle ayrılmış listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1107b-126">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1107b-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1107b-127">-PassThru</span></span>
<span data-ttu-id="1107b-128">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="1107b-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1107b-129">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="1107b-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1107b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1107b-130">-ResourceGroupName</span></span>
<span data-ttu-id="1107b-131">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1107b-131">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1107b-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1107b-132">-RetentionInDays</span></span>
<span data-ttu-id="1107b-133">Denetim günlükleri için bekletme günü sayısı</span><span class="sxs-lookup"><span data-stu-id="1107b-133">The number of retention days for the audit logs</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1107b-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1107b-134">-ServerName</span></span>
<span data-ttu-id="1107b-135">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1107b-135">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1107b-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1107b-136">-StorageAccountName</span></span>
<span data-ttu-id="1107b-137">Kullanılacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1107b-137">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="1107b-138">Joker karakterlere izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="1107b-138">Wildcards are not permitted.</span></span> <span data-ttu-id="1107b-139">Bu parametre gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="1107b-139">This parameter is not required.</span></span> <span data-ttu-id="1107b-140">Bu parametre sağlanmadıysa cmdlet, veritabanının tehdit algılama ilkesinin bir parçası olarak daha önce tanımlanan depolama hesabını kullanır.</span><span class="sxs-lookup"><span data-stu-id="1107b-140">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="1107b-141">Bir veritabanı tehdit algılama ilkesi ilk kez tanımlandıysa ve bu parametre sağlanmadıysa cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="1107b-141">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1107b-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="1107b-142">-Confirm</span></span>
<span data-ttu-id="1107b-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1107b-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1107b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1107b-144">-WhatIf</span></span>
<span data-ttu-id="1107b-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1107b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1107b-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1107b-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1107b-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1107b-147">-DefaultProfile</span></span>
<span data-ttu-id="1107b-148">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1107b-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1107b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1107b-149">CommonParameters</span></span>
<span data-ttu-id="1107b-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1107b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1107b-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1107b-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1107b-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1107b-152">INPUTS</span></span>

###  
<span data-ttu-id="1107b-153">Bu cmdlet 'e giriş kanalı oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="1107b-153">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="1107b-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1107b-154">OUTPUTS</span></span>

### <span data-ttu-id="1107b-155">Microsoft. Azure. Commands. Sql. ThreatDetection. model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="1107b-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="1107b-156">Bu cmdlet, bir **model. DatabaseThreatDetectionPolicyModel** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="1107b-156">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="1107b-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1107b-157">NOTES</span></span>

## <span data-ttu-id="1107b-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1107b-158">RELATED LINKS</span></span>

[<span data-ttu-id="1107b-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1107b-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="1107b-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1107b-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="1107b-161">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="1107b-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


