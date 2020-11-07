---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 4b63568b4a2bfd6b79c51fcd906819f4831a7ade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763607"
---
# <span data-ttu-id="b3e06-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="b3e06-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="b3e06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3e06-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e06-103">Sunucu uzun bekletme Kasası alır.</span><span class="sxs-lookup"><span data-stu-id="b3e06-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3e06-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3e06-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3e06-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3e06-105">DESCRIPTION</span></span>
<span data-ttu-id="b3e06-106">**Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet 'i, bu sunucuya kaydedilen uzun süreli bekletme kasasından alır.</span><span class="sxs-lookup"><span data-stu-id="b3e06-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="b3e06-107">Kasa, yedek verileri depolamak için kullanılan bir Azure yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="b3e06-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="b3e06-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3e06-108">EXAMPLES</span></span>

## <span data-ttu-id="b3e06-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3e06-109">PARAMETERS</span></span>

### <span data-ttu-id="b3e06-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3e06-110">-ResourceGroupName</span></span>
<span data-ttu-id="b3e06-111">Sunucuyu içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3e06-111">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="b3e06-112">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b3e06-112">-ServerName</span></span>
<span data-ttu-id="b3e06-113">Bu cmdlet 'in kasa aldığı sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3e06-113">Specifies the server for which this cmdlet gets a vault.</span></span>

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

### <span data-ttu-id="b3e06-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="b3e06-114">-Confirm</span></span>
<span data-ttu-id="b3e06-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b3e06-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3e06-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3e06-116">-WhatIf</span></span>
<span data-ttu-id="b3e06-117">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3e06-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3e06-118">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b3e06-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3e06-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e06-119">-DefaultProfile</span></span>
<span data-ttu-id="b3e06-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3e06-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3e06-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e06-121">CommonParameters</span></span>
<span data-ttu-id="b3e06-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3e06-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e06-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3e06-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e06-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3e06-124">INPUTS</span></span>

## <span data-ttu-id="b3e06-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3e06-125">OUTPUTS</span></span>

## <span data-ttu-id="b3e06-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3e06-126">NOTES</span></span>

## <span data-ttu-id="b3e06-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3e06-127">RELATED LINKS</span></span>

[<span data-ttu-id="b3e06-128">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="b3e06-128">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="b3e06-129">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="b3e06-129">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

