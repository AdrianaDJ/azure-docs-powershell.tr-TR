---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7642F18A-B193-4849-BE3C-1B85FBD213F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: e76ba16f9578eefdce36a1f3d726e027be2a9ed6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594331"
---
# <span data-ttu-id="83e8b-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="83e8b-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="83e8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83e8b-102">SYNOPSIS</span></span>
<span data-ttu-id="83e8b-103">Sunucu uzun bekletme Kasası ayarlar.</span><span class="sxs-lookup"><span data-stu-id="83e8b-103">Sets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83e8b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83e8b-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerBackupLongTermRetentionVault -ResourceId <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83e8b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="83e8b-105">DESCRIPTION</span></span>
<span data-ttu-id="83e8b-106">**Set-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet 'i, bu sunucuya kaydedilen uzun süreli bekletme kasasıyla ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="83e8b-106">The **Set-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet sets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="83e8b-107">Kasa, yedek verileri depolamak için kullanılan bir Azure yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="83e8b-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="83e8b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83e8b-108">EXAMPLES</span></span>

## <span data-ttu-id="83e8b-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83e8b-109">PARAMETERS</span></span>

### <span data-ttu-id="83e8b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e8b-110">-DefaultProfile</span></span>
<span data-ttu-id="83e8b-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="83e8b-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83e8b-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83e8b-112">-ResourceGroupName</span></span>
<span data-ttu-id="83e8b-113">Sunucuyu içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83e8b-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="83e8b-114">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="83e8b-114">-ResourceId</span></span>
<span data-ttu-id="83e8b-115">Kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="83e8b-115">Specifies the ID of a resource.</span></span>

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

### <span data-ttu-id="83e8b-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="83e8b-116">-ServerName</span></span>
<span data-ttu-id="83e8b-117">Bu cmdlet 'in kasa ayarladığı sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="83e8b-117">Specifies the server for which this cmdlet sets a vault.</span></span>

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

### <span data-ttu-id="83e8b-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="83e8b-118">-Confirm</span></span>
<span data-ttu-id="83e8b-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="83e8b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83e8b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83e8b-120">-WhatIf</span></span>
<span data-ttu-id="83e8b-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="83e8b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83e8b-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="83e8b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83e8b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e8b-123">CommonParameters</span></span>
<span data-ttu-id="83e8b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83e8b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e8b-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83e8b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e8b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83e8b-126">INPUTS</span></span>

### <span data-ttu-id="83e8b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="83e8b-127">System.String</span></span>

## <span data-ttu-id="83e8b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83e8b-128">OUTPUTS</span></span>

### <span data-ttu-id="83e8b-129">Microsoft. Azure. Commands. Sql. Backup. model. AzureSqlServerBackupLongTermRetentionVaultModel</span><span class="sxs-lookup"><span data-stu-id="83e8b-129">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlServerBackupLongTermRetentionVaultModel</span></span>

## <span data-ttu-id="83e8b-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83e8b-130">NOTES</span></span>

## <span data-ttu-id="83e8b-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83e8b-131">RELATED LINKS</span></span>

[<span data-ttu-id="83e8b-132">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="83e8b-132">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Get-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="83e8b-133">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="83e8b-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)