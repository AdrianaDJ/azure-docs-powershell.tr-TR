---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 0aeee8e991d0f74a341a750e69016b12027fe584
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590829"
---
# <span data-ttu-id="5fc27-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="5fc27-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="5fc27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fc27-102">SYNOPSIS</span></span>
<span data-ttu-id="5fc27-103">Sunucu uzun bekletme Kasası alır.</span><span class="sxs-lookup"><span data-stu-id="5fc27-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fc27-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5fc27-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fc27-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5fc27-105">DESCRIPTION</span></span>
<span data-ttu-id="5fc27-106">**Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet 'i, bu sunucuya kaydedilen uzun süreli bekletme kasasından alır.</span><span class="sxs-lookup"><span data-stu-id="5fc27-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="5fc27-107">Kasa, yedek verileri depolamak için kullanılan bir Azure yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="5fc27-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="5fc27-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5fc27-108">EXAMPLES</span></span>

## <span data-ttu-id="5fc27-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5fc27-109">PARAMETERS</span></span>

### <span data-ttu-id="5fc27-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fc27-110">-DefaultProfile</span></span>
<span data-ttu-id="5fc27-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5fc27-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fc27-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fc27-112">-ResourceGroupName</span></span>
<span data-ttu-id="5fc27-113">Sunucuyu içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fc27-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="5fc27-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5fc27-114">-ServerName</span></span>
<span data-ttu-id="5fc27-115">Bu cmdlet 'in kasa aldığı sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fc27-115">Specifies the server for which this cmdlet gets a vault.</span></span>

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

### <span data-ttu-id="5fc27-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="5fc27-116">-Confirm</span></span>
<span data-ttu-id="5fc27-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5fc27-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fc27-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fc27-118">-WhatIf</span></span>
<span data-ttu-id="5fc27-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5fc27-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fc27-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5fc27-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fc27-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fc27-121">CommonParameters</span></span>
<span data-ttu-id="5fc27-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5fc27-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fc27-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fc27-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fc27-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5fc27-124">INPUTS</span></span>

### <span data-ttu-id="5fc27-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5fc27-125">System.String</span></span>

## <span data-ttu-id="5fc27-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5fc27-126">OUTPUTS</span></span>

### <span data-ttu-id="5fc27-127">Microsoft. Azure. Commands. Sql. Backup. model. AzureSqlServerBackupLongTermRetentionVaultModel</span><span class="sxs-lookup"><span data-stu-id="5fc27-127">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlServerBackupLongTermRetentionVaultModel</span></span>

## <span data-ttu-id="5fc27-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5fc27-128">NOTES</span></span>

## <span data-ttu-id="5fc27-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5fc27-129">RELATED LINKS</span></span>

[<span data-ttu-id="5fc27-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="5fc27-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="5fc27-131">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="5fc27-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
