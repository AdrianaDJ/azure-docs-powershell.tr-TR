---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 0492b81e5674ea08ad98dff1fca75335b1ec8fa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591568"
---
# <span data-ttu-id="e65d3-101">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e65d3-101">New-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="e65d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e65d3-102">SYNOPSIS</span></span>
<span data-ttu-id="e65d3-103">İki SQL veritabanı sunucusu arasındaki elastik veritabanı işlemleri için iletişim bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e65d3-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e65d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e65d3-104">SYNTAX</span></span>

```
New-AzureRmSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e65d3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e65d3-105">DESCRIPTION</span></span>
<span data-ttu-id="e65d3-106">**Yeni-AzureRmSqlServerCommunicationLink** cmdlet 'ı, Azure SQL veritabanında iki mantıksal sunucu arasındaki elastik veritabanı işlemleri için iletişim bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e65d3-106">The **New-AzureRmSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="e65d3-107">Elastik veritabanı işlemleri eşlenmiş sunuculardan herhangi birinin veritabanına yayılabilir.</span><span class="sxs-lookup"><span data-stu-id="e65d3-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="e65d3-108">Bir sunucuda birden çok bağlantı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e65d3-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="e65d3-109">Bu nedenle, elastik veritabanı işlemleri daha fazla sayıda sunucuya yayılabilir.</span><span class="sxs-lookup"><span data-stu-id="e65d3-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="e65d3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e65d3-110">EXAMPLES</span></span>

### <span data-ttu-id="e65d3-111">Örnek 1: iletişim bağlantısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="e65d3-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="e65d3-112">Bu komut ContosoServer17 ve ContosoServer02 arasında Link01 adlı bir bağlantı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e65d3-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="e65d3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e65d3-113">PARAMETERS</span></span>

### <span data-ttu-id="e65d3-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="e65d3-114">-AsJob</span></span>
<span data-ttu-id="e65d3-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e65d3-115">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="e65d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e65d3-116">-DefaultProfile</span></span>
<span data-ttu-id="e65d3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e65d3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e65d3-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="e65d3-118">-LinkName</span></span>
<span data-ttu-id="e65d3-119">Bu cmdlet 'in oluşturduğu sunucu iletişim bağlantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e65d3-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e65d3-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="e65d3-120">-PartnerServer</span></span>
<span data-ttu-id="e65d3-121">Bu iletişim bağlantısında yer alan diğer sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e65d3-121">Specifies the name of the other server that takes part in this communication link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e65d3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e65d3-122">-ResourceGroupName</span></span>
<span data-ttu-id="e65d3-123">*ServerName* parametresi tarafından belirtilen sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e65d3-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="e65d3-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e65d3-124">-ServerName</span></span>
<span data-ttu-id="e65d3-125">Bu cmdlet 'in iletişim bağlantısını ayarladığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e65d3-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="e65d3-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="e65d3-126">-Confirm</span></span>
<span data-ttu-id="e65d3-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e65d3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e65d3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e65d3-128">-WhatIf</span></span>
<span data-ttu-id="e65d3-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e65d3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e65d3-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e65d3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e65d3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e65d3-131">CommonParameters</span></span>
<span data-ttu-id="e65d3-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e65d3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e65d3-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e65d3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e65d3-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e65d3-134">INPUTS</span></span>

### <span data-ttu-id="e65d3-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e65d3-135">None</span></span>
<span data-ttu-id="e65d3-136">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e65d3-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e65d3-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e65d3-137">OUTPUTS</span></span>

### <span data-ttu-id="e65d3-138">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservercommunicationlinkmodel</span><span class="sxs-lookup"><span data-stu-id="e65d3-138">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="e65d3-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e65d3-139">NOTES</span></span>
* <span data-ttu-id="e65d3-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL</span><span class="sxs-lookup"><span data-stu-id="e65d3-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="e65d3-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e65d3-141">RELATED LINKS</span></span>

[<span data-ttu-id="e65d3-142">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e65d3-142">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="e65d3-143">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e65d3-143">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="e65d3-144">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="e65d3-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
