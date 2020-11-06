---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 5ee1039f938c561424ded9768e9d5f84372410fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573170"
---
# <span data-ttu-id="96c25-101">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="96c25-101">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="96c25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96c25-102">SYNOPSIS</span></span>
<span data-ttu-id="96c25-103">Sunucu için tehdit algılama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="96c25-103">Gets the threat detection policy for a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96c25-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96c25-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96c25-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="96c25-105">DESCRIPTION</span></span>
<span data-ttu-id="96c25-106">**Get-AzureRmSqlServerThreatDetectionPolicy** cmdlet 'ı BIR Azure SQL Server 'ın tehdit algılama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="96c25-106">The **Get-AzureRmSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="96c25-107">Bu cmdlet 'i kullanmak için, bu cmdlet 'in ilkeyi aldığı sunucuyu tanımlayacak *Resourcegroupname* ve *ServerName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="96c25-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="96c25-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96c25-108">EXAMPLES</span></span>

### <span data-ttu-id="96c25-109">Örnek 1: sunucunun tehdit algılama ilkesini alma</span><span class="sxs-lookup"><span data-stu-id="96c25-109">Example 1: Get the threat detection policy for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="96c25-110">Bu komut, server01 adlı bir sunucuda tehdit algılama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="96c25-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="96c25-111">Sunucu, ResourceGroup11 kaynak grubuna atanır.</span><span class="sxs-lookup"><span data-stu-id="96c25-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="96c25-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96c25-112">PARAMETERS</span></span>

### <span data-ttu-id="96c25-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c25-113">-DefaultProfile</span></span>
<span data-ttu-id="96c25-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="96c25-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96c25-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96c25-115">-ResourceGroupName</span></span>
<span data-ttu-id="96c25-116">Sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96c25-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="96c25-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="96c25-117">-ServerName</span></span>
<span data-ttu-id="96c25-118">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96c25-118">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c25-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="96c25-119">-Confirm</span></span>
<span data-ttu-id="96c25-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="96c25-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96c25-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96c25-121">-WhatIf</span></span>
<span data-ttu-id="96c25-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="96c25-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96c25-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="96c25-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96c25-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c25-124">CommonParameters</span></span>
<span data-ttu-id="96c25-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96c25-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c25-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96c25-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c25-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96c25-127">INPUTS</span></span>

### <span data-ttu-id="96c25-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="96c25-128">None</span></span>
<span data-ttu-id="96c25-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="96c25-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="96c25-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96c25-130">OUTPUTS</span></span>

### <span data-ttu-id="96c25-131">Microsoft. Azure. Commands. Sql. ThreatDetection. model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="96c25-131">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="96c25-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96c25-132">NOTES</span></span>

## <span data-ttu-id="96c25-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96c25-133">RELATED LINKS</span></span>

[<span data-ttu-id="96c25-134">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="96c25-134">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="96c25-135">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="96c25-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


