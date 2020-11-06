---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1C0AF5B2-7187-4BFA-8DBB-A771FD2E00A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: a4538210c95f8357a9b920f827e8812b47377a2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589054"
---
# <span data-ttu-id="968bf-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="968bf-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="968bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="968bf-102">SYNOPSIS</span></span>
<span data-ttu-id="968bf-103">Bir veritabanı uzun bekletme ilkesi alır.</span><span class="sxs-lookup"><span data-stu-id="968bf-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="968bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="968bf-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="968bf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="968bf-105">DESCRIPTION</span></span>
<span data-ttu-id="968bf-106">**Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet 'i, bu veritabanına kaydedilen uzun süreli bekletme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="968bf-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="968bf-107">İlke, yedek depolama ilkesini tanımlamak için kullanılan bir Azure yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="968bf-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="968bf-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="968bf-108">EXAMPLES</span></span>

## <span data-ttu-id="968bf-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="968bf-109">PARAMETERS</span></span>

### <span data-ttu-id="968bf-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="968bf-110">-DatabaseName</span></span>
<span data-ttu-id="968bf-111">Bu cmdlet 'in ilkeyi aldığı SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="968bf-111">Specifies the name of the SQL Database for which this cmdlet gets a policy.</span></span>

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

### <span data-ttu-id="968bf-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="968bf-112">-ResourceGroupName</span></span>
<span data-ttu-id="968bf-113">Veritabanını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="968bf-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="968bf-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="968bf-114">-ServerName</span></span>
<span data-ttu-id="968bf-115">Veritabanını barındıran sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="968bf-115">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="968bf-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="968bf-116">-Confirm</span></span>
<span data-ttu-id="968bf-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="968bf-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="968bf-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="968bf-118">-WhatIf</span></span>
<span data-ttu-id="968bf-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="968bf-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="968bf-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="968bf-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="968bf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="968bf-121">-DefaultProfile</span></span>
<span data-ttu-id="968bf-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="968bf-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="968bf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="968bf-123">CommonParameters</span></span>
<span data-ttu-id="968bf-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="968bf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="968bf-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="968bf-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="968bf-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="968bf-126">INPUTS</span></span>

## <span data-ttu-id="968bf-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="968bf-127">OUTPUTS</span></span>

## <span data-ttu-id="968bf-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="968bf-128">NOTES</span></span>

## <span data-ttu-id="968bf-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="968bf-129">RELATED LINKS</span></span>

[<span data-ttu-id="968bf-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="968bf-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="968bf-131">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="968bf-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
