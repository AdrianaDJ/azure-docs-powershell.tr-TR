---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 567cb47599a23bf83581afb97a425902ee0e159a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588742"
---
# <span data-ttu-id="dd3c9-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="dd3c9-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="dd3c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd3c9-102">SYNOPSIS</span></span>
<span data-ttu-id="dd3c9-103">Sunucu uzun bekletme Kasası alır.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd3c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd3c9-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd3c9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd3c9-105">DESCRIPTION</span></span>
<span data-ttu-id="dd3c9-106">**Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet 'i, bu sunucuya kaydedilen uzun süreli bekletme kasasından alır.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="dd3c9-107">Kasa, yedek verileri depolamak için kullanılan bir Azure yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="dd3c9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd3c9-108">EXAMPLES</span></span>

## <span data-ttu-id="dd3c9-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd3c9-109">PARAMETERS</span></span>

### <span data-ttu-id="dd3c9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd3c9-110">-DefaultProfile</span></span>
<span data-ttu-id="dd3c9-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="dd3c9-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd3c9-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd3c9-112">-ResourceGroupName</span></span>
<span data-ttu-id="dd3c9-113">Sunucuyu içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="dd3c9-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dd3c9-114">-ServerName</span></span>
<span data-ttu-id="dd3c9-115">Bu cmdlet 'in kasa aldığı sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-115">Specifies the server for which this cmdlet gets a vault.</span></span>

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

### <span data-ttu-id="dd3c9-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="dd3c9-116">-Confirm</span></span>
<span data-ttu-id="dd3c9-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd3c9-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd3c9-118">-WhatIf</span></span>
<span data-ttu-id="dd3c9-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd3c9-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd3c9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd3c9-121">CommonParameters</span></span>
<span data-ttu-id="dd3c9-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd3c9-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd3c9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd3c9-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd3c9-124">INPUTS</span></span>

### <span data-ttu-id="dd3c9-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dd3c9-125">None</span></span>
<span data-ttu-id="dd3c9-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dd3c9-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd3c9-127">OUTPUTS</span></span>

## <span data-ttu-id="dd3c9-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd3c9-128">NOTES</span></span>

## <span data-ttu-id="dd3c9-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd3c9-129">RELATED LINKS</span></span>

[<span data-ttu-id="dd3c9-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="dd3c9-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="dd3c9-131">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="dd3c9-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

