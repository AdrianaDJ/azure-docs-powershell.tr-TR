---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: ed968db32505bcb3c581775d05235cc4c718dd67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592168"
---
# <span data-ttu-id="b03c8-101">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="b03c8-101">Get-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="b03c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b03c8-102">SYNOPSIS</span></span>
<span data-ttu-id="b03c8-103">Veritabanı sunucuları arasındaki elastik veritabanı işlemleri için iletişim bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="b03c8-103">Gets communication links for elastic database transactions between database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b03c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b03c8-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b03c8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b03c8-105">DESCRIPTION</span></span>
<span data-ttu-id="b03c8-106">**Get-AzureRmSqlServerCommunicationLink** cmdlet 'ı, Azure SQL veritabanındaki elastik veritabanı işlemleri için sunucudan sunucuya iletişim bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="b03c8-106">The **Get-AzureRmSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="b03c8-107">Bağlantının özelliklerini görmek için sunucu iletişim bağlantısının adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b03c8-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="b03c8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b03c8-108">EXAMPLES</span></span>

### <span data-ttu-id="b03c8-109">Örnek 1: sunucunun tüm iletişim bağlantılarını alma</span><span class="sxs-lookup"><span data-stu-id="b03c8-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="b03c8-110">Bu komut, ContosoServer17 adlı sunucudaki elastik veritabanı işlemleri için tüm sunucudan sunucuya iletişim bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="b03c8-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="b03c8-111">Örnek 2: sunucu için belirli bir iletişim bağlantısı alma</span><span class="sxs-lookup"><span data-stu-id="b03c8-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="b03c8-112">Bu komut, Link01 adlı sunucudan sunucuya iletişim bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="b03c8-112">This command gets the server-to-server communication link named Link01.</span></span>

## <span data-ttu-id="b03c8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b03c8-113">PARAMETERS</span></span>

### <span data-ttu-id="b03c8-114">-LinkName</span><span class="sxs-lookup"><span data-stu-id="b03c8-114">-LinkName</span></span>
<span data-ttu-id="b03c8-115">Bu cmdlet 'in aldığı sunucu iletişim bağlantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b03c8-115">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b03c8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b03c8-116">-ResourceGroupName</span></span>
<span data-ttu-id="b03c8-117">*ServerName* parametresi tarafından belirtilen sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b03c8-117">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="b03c8-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b03c8-118">-ServerName</span></span>
<span data-ttu-id="b03c8-119">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b03c8-119">Specifies the name of a server.</span></span>
<span data-ttu-id="b03c8-120">Bu sunucu, bu cmdlet 'in aldığı iletişim bağlantısını içerir.</span><span class="sxs-lookup"><span data-stu-id="b03c8-120">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b03c8-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="b03c8-121">-Confirm</span></span>
<span data-ttu-id="b03c8-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b03c8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b03c8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b03c8-123">-WhatIf</span></span>
<span data-ttu-id="b03c8-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b03c8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b03c8-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b03c8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b03c8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b03c8-126">-DefaultProfile</span></span>
<span data-ttu-id="b03c8-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b03c8-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b03c8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b03c8-128">CommonParameters</span></span>
<span data-ttu-id="b03c8-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b03c8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b03c8-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b03c8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b03c8-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b03c8-131">INPUTS</span></span>

## <span data-ttu-id="b03c8-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b03c8-132">OUTPUTS</span></span>

### <span data-ttu-id="b03c8-133">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservercommunicationlinkmodel</span><span class="sxs-lookup"><span data-stu-id="b03c8-133">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="b03c8-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b03c8-134">NOTES</span></span>
* <span data-ttu-id="b03c8-135">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL</span><span class="sxs-lookup"><span data-stu-id="b03c8-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="b03c8-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b03c8-136">RELATED LINKS</span></span>

[<span data-ttu-id="b03c8-137">Yeni-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="b03c8-137">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="b03c8-138">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="b03c8-138">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="b03c8-139">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="b03c8-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
