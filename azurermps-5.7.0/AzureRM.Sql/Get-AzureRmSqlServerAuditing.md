---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 636b3602c6dafc2c00e02e19aa35d0e91c278137
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588745"
---
# <span data-ttu-id="b70c4-101">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="b70c4-101">Get-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="b70c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b70c4-102">SYNOPSIS</span></span>
<span data-ttu-id="b70c4-103">Bir Azure SQL Server 'ın denetim ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b70c4-103">Gets the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b70c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b70c4-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditing [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b70c4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b70c4-105">DESCRIPTION</span></span>
<span data-ttu-id="b70c4-106">**Get-AzureRmSqlServerAuditing** cmdlet 'i, BIR Azure SQL Server 'ın blob denetim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="b70c4-106">The **Get-AzureRmSqlServerAuditing** cmdlet gets the blob auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="b70c4-107">Veritabanını tanımlamak için *Resourcegroupname* ve *ServerName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b70c4-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the database.</span></span>
<span data-ttu-id="b70c4-108">Bu cmdlet, belirtilen Azure SQL Server 'da tanımlanan Azure SQL veritabanları tarafından kullanılan bir ilkeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="b70c4-108">This cmdlet returns a policy that is used by the Azure SQL databases that are defined in the specified Azure SQL server.</span></span>

## <span data-ttu-id="b70c4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b70c4-109">EXAMPLES</span></span>

### <span data-ttu-id="b70c4-110">Örnek 1: Azure SQL Server 'ın denetim ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="b70c4-110">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...}
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="b70c4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b70c4-111">PARAMETERS</span></span>

### <span data-ttu-id="b70c4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b70c4-112">-DefaultProfile</span></span>
<span data-ttu-id="b70c4-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b70c4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b70c4-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b70c4-114">-ResourceGroupName</span></span>
<span data-ttu-id="b70c4-115">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b70c4-115">The name of the resource group.</span></span>

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

### <span data-ttu-id="b70c4-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b70c4-116">-ServerName</span></span>
<span data-ttu-id="b70c4-117">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="b70c4-117">SQL server name.</span></span>

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

### <span data-ttu-id="b70c4-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="b70c4-118">-Confirm</span></span>
<span data-ttu-id="b70c4-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b70c4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b70c4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b70c4-120">-WhatIf</span></span>
<span data-ttu-id="b70c4-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b70c4-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b70c4-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b70c4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b70c4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b70c4-123">CommonParameters</span></span>
<span data-ttu-id="b70c4-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b70c4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b70c4-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b70c4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b70c4-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b70c4-126">INPUTS</span></span>

### <span data-ttu-id="b70c4-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b70c4-127">None</span></span>
<span data-ttu-id="b70c4-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b70c4-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b70c4-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b70c4-129">OUTPUTS</span></span>

### <span data-ttu-id="b70c4-130">Microsoft. Azure. Commands. Sql. Security. model. Serverblobobauditingsettingsmodel</span><span class="sxs-lookup"><span data-stu-id="b70c4-130">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="b70c4-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b70c4-131">NOTES</span></span>

## <span data-ttu-id="b70c4-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b70c4-132">RELATED LINKS</span></span>
