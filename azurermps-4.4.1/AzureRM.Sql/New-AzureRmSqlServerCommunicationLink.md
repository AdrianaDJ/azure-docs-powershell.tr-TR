---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: ac2ec676143ef1179adbfeb793bd787d81e8f435
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587749"
---
# <span data-ttu-id="7ba6a-101">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="7ba6a-101">New-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="7ba6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ba6a-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba6a-103">İki SQL veritabanı sunucusu arasındaki elastik veritabanı işlemleri için iletişim bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7ba6a-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ba6a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ba6a-104">SYNTAX</span></span>

```
New-AzureRmSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ba6a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ba6a-105">DESCRIPTION</span></span>
<span data-ttu-id="7ba6a-106">**Yeni-AzureRmSqlServerCommunicationLink** cmdlet 'ı, Azure SQL veritabanında iki mantıksal sunucu arasındaki elastik veritabanı işlemleri için iletişim bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7ba6a-106">The **New-AzureRmSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="7ba6a-107">Elastik veritabanı işlemleri eşlenmiş sunuculardan herhangi birinin veritabanına yayılabilir.</span><span class="sxs-lookup"><span data-stu-id="7ba6a-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="7ba6a-108">Bir sunucuda birden çok bağlantı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7ba6a-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="7ba6a-109">Bu nedenle, elastik veritabanı işlemleri daha fazla sayıda sunucuya yayılabilir.</span><span class="sxs-lookup"><span data-stu-id="7ba6a-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="7ba6a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ba6a-110">EXAMPLES</span></span>

### <span data-ttu-id="7ba6a-111">Örnek 1: iletişim bağlantısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="7ba6a-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="7ba6a-112">Bu komut ContosoServer17 ve ContosoServer02 arasında Link01 adlı bir bağlantı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7ba6a-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="7ba6a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ba6a-113">PARAMETERS</span></span>

### <span data-ttu-id="7ba6a-114">-LinkName</span><span class="sxs-lookup"><span data-stu-id="7ba6a-114">-LinkName</span></span>
<span data-ttu-id="7ba6a-115">Bu cmdlet 'in oluşturduğu sunucu iletişim bağlantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ba6a-115">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7ba6a-116">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="7ba6a-116">-PartnerServer</span></span>
<span data-ttu-id="7ba6a-117">Bu iletişim bağlantısında yer alan diğer sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ba6a-117">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="7ba6a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ba6a-118">-ResourceGroupName</span></span>
<span data-ttu-id="7ba6a-119">*ServerName* parametresi tarafından belirtilen sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ba6a-119">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="7ba6a-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7ba6a-120">-ServerName</span></span>
<span data-ttu-id="7ba6a-121">Bu cmdlet 'in iletişim bağlantısını ayarladığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ba6a-121">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="7ba6a-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="7ba6a-122">-Confirm</span></span>
<span data-ttu-id="7ba6a-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7ba6a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ba6a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ba6a-124">-WhatIf</span></span>
<span data-ttu-id="7ba6a-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7ba6a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ba6a-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7ba6a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ba6a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba6a-127">-DefaultProfile</span></span>
<span data-ttu-id="7ba6a-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7ba6a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ba6a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba6a-129">CommonParameters</span></span>
<span data-ttu-id="7ba6a-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ba6a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba6a-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ba6a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba6a-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ba6a-132">INPUTS</span></span>

## <span data-ttu-id="7ba6a-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ba6a-133">OUTPUTS</span></span>

### <span data-ttu-id="7ba6a-134">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservercommunicationlinkmodel</span><span class="sxs-lookup"><span data-stu-id="7ba6a-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="7ba6a-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ba6a-135">NOTES</span></span>
* <span data-ttu-id="7ba6a-136">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL</span><span class="sxs-lookup"><span data-stu-id="7ba6a-136">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="7ba6a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ba6a-137">RELATED LINKS</span></span>

[<span data-ttu-id="7ba6a-138">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="7ba6a-138">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="7ba6a-139">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="7ba6a-139">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="7ba6a-140">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="7ba6a-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
