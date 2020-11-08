---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: ad3c257366513a5cc9998b4e4edea8879dc38545
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266300"
---
# <span data-ttu-id="5b1ee-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="5b1ee-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="5b1ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b1ee-102">SYNOPSIS</span></span>
<span data-ttu-id="5b1ee-103">Veritabanı sunucusu sistem kurtarma yapılandırması için etkinlik alır.</span><span class="sxs-lookup"><span data-stu-id="5b1ee-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="5b1ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b1ee-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b1ee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b1ee-105">DESCRIPTION</span></span>
<span data-ttu-id="5b1ee-106">**Get-Azsqlserverdeyıldız Recoveryconfigurationactivity** CMDLET 'i SQL veritabanı sunucusu sistem kurtarma yapılandırması için etkinlik alır.</span><span class="sxs-lookup"><span data-stu-id="5b1ee-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="5b1ee-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b1ee-107">EXAMPLES</span></span>

## <span data-ttu-id="5b1ee-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b1ee-108">PARAMETERS</span></span>

### <span data-ttu-id="5b1ee-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b1ee-109">-DefaultProfile</span></span>
<span data-ttu-id="5b1ee-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5b1ee-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b1ee-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5b1ee-111">-OperationId</span></span>
<span data-ttu-id="5b1ee-112">İşlem KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b1ee-112">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1ee-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b1ee-113">-ResourceGroupName</span></span>
<span data-ttu-id="5b1ee-114">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b1ee-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5b1ee-115">-Serverdisderecoveryconfigurationname</span><span class="sxs-lookup"><span data-stu-id="5b1ee-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="5b1ee-116">Sunucu sistem kurtarma yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b1ee-116">Specifies the name of the server system recovery configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1ee-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5b1ee-117">-ServerName</span></span>
<span data-ttu-id="5b1ee-118">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b1ee-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="5b1ee-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="5b1ee-119">-Confirm</span></span>
<span data-ttu-id="5b1ee-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5b1ee-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b1ee-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b1ee-121">-WhatIf</span></span>
<span data-ttu-id="5b1ee-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b1ee-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b1ee-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5b1ee-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b1ee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b1ee-124">CommonParameters</span></span>
<span data-ttu-id="5b1ee-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b1ee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b1ee-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5b1ee-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b1ee-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b1ee-127">INPUTS</span></span>

### <span data-ttu-id="5b1ee-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5b1ee-128">System.String</span></span>

### <span data-ttu-id="5b1ee-129">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="5b1ee-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5b1ee-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b1ee-130">OUTPUTS</span></span>

### <span data-ttu-id="5b1ee-131">Microsoft. Azure. Commands. Sql. Serverdeyıldız yapılandırması. model. Azuresbir</span><span class="sxs-lookup"><span data-stu-id="5b1ee-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="5b1ee-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b1ee-132">NOTES</span></span>

## <span data-ttu-id="5b1ee-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b1ee-133">RELATED LINKS</span></span>

[<span data-ttu-id="5b1ee-134">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="5b1ee-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
