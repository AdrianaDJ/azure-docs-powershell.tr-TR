---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 196E1AC9-A1E2-47D2-A3C1-535EFE439EE8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 1bfe5d721930288c65a18be8ccba2ebfe2f90484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590604"
---
# <span data-ttu-id="1e3aa-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1e3aa-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="1e3aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e3aa-102">SYNOPSIS</span></span>
<span data-ttu-id="1e3aa-103">Sunucu uzun bekletme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1e3aa-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e3aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e3aa-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e3aa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e3aa-105">DESCRIPTION</span></span>
<span data-ttu-id="1e3aa-106">**Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet 'i, bu veritabanına kaydedilen uzun süreli bekletme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1e3aa-106">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="1e3aa-107">İlke, yedek depolama ilkesini tanımlamak için kullanılan bir Azure yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="1e3aa-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="1e3aa-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e3aa-108">EXAMPLES</span></span>

## <span data-ttu-id="1e3aa-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e3aa-109">PARAMETERS</span></span>

### <span data-ttu-id="1e3aa-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1e3aa-110">-DatabaseName</span></span>
<span data-ttu-id="1e3aa-111">Bu cmdlet 'in ilke ayarladığı SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e3aa-111">Specifies the name of the SQL Database for which this cmdlet sets a policy.</span></span>

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

### <span data-ttu-id="1e3aa-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e3aa-112">-ResourceGroupName</span></span>
<span data-ttu-id="1e3aa-113">Veritabanını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e3aa-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="1e3aa-114">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1e3aa-114">-ResourceId</span></span>
<span data-ttu-id="1e3aa-115">Kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e3aa-115">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e3aa-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1e3aa-116">-ServerName</span></span>
<span data-ttu-id="1e3aa-117">Veritabanını barındıran sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e3aa-117">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="1e3aa-118">Durumlu</span><span class="sxs-lookup"><span data-stu-id="1e3aa-118">-State</span></span>
<span data-ttu-id="1e3aa-119">Bir durumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e3aa-119">Specifies a state.</span></span>

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

### <span data-ttu-id="1e3aa-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="1e3aa-120">-Confirm</span></span>
<span data-ttu-id="1e3aa-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1e3aa-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e3aa-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e3aa-122">-WhatIf</span></span>
<span data-ttu-id="1e3aa-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1e3aa-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e3aa-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1e3aa-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e3aa-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e3aa-125">-DefaultProfile</span></span>
<span data-ttu-id="1e3aa-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e3aa-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e3aa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e3aa-127">CommonParameters</span></span>
<span data-ttu-id="1e3aa-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e3aa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e3aa-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e3aa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e3aa-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e3aa-130">INPUTS</span></span>

## <span data-ttu-id="1e3aa-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e3aa-131">OUTPUTS</span></span>

## <span data-ttu-id="1e3aa-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e3aa-132">NOTES</span></span>

## <span data-ttu-id="1e3aa-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e3aa-133">RELATED LINKS</span></span>

[<span data-ttu-id="1e3aa-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1e3aa-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="1e3aa-135">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="1e3aa-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
