---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 508a19b51fea8435ec48e060e63ee3b3cecc5f65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590005"
---
# <span data-ttu-id="d0421-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="d0421-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="d0421-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0421-102">SYNOPSIS</span></span>
<span data-ttu-id="d0421-103">Veritabanı sunucusu sistem kurtarma yapılandırması için etkinlik alır.</span><span class="sxs-lookup"><span data-stu-id="d0421-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0421-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d0421-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0421-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0421-105">DESCRIPTION</span></span>
<span data-ttu-id="d0421-106">**Get-Azurermsqlserverdisderecoveryconfigurationactivity** CMDLET 'i SQL veritabanı sunucusu sistem kurtarma yapılandırması için etkinlik alır.</span><span class="sxs-lookup"><span data-stu-id="d0421-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="d0421-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d0421-107">EXAMPLES</span></span>

## <span data-ttu-id="d0421-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d0421-108">PARAMETERS</span></span>

### <span data-ttu-id="d0421-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0421-109">-DefaultProfile</span></span>
<span data-ttu-id="d0421-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d0421-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0421-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d0421-111">-OperationId</span></span>
<span data-ttu-id="d0421-112">İşlem KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0421-112">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="d0421-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0421-113">-ResourceGroupName</span></span>
<span data-ttu-id="d0421-114">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0421-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d0421-115">-Serverdisderecoveryconfigurationname</span><span class="sxs-lookup"><span data-stu-id="d0421-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="d0421-116">Sunucu sistem kurtarma yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0421-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="d0421-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d0421-117">-ServerName</span></span>
<span data-ttu-id="d0421-118">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0421-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="d0421-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="d0421-119">-Confirm</span></span>
<span data-ttu-id="d0421-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d0421-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0421-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0421-121">-WhatIf</span></span>
<span data-ttu-id="d0421-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d0421-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0421-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d0421-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0421-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0421-124">CommonParameters</span></span>
<span data-ttu-id="d0421-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d0421-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0421-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0421-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0421-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d0421-127">INPUTS</span></span>

### <span data-ttu-id="d0421-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d0421-128">System.String</span></span>

### <span data-ttu-id="d0421-129">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d0421-129">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d0421-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d0421-130">OUTPUTS</span></span>

### <span data-ttu-id="d0421-131">Microsoft. Azure. Commands. Sql. Serverdeyıldız yapılandırması. model. Azuresbir</span><span class="sxs-lookup"><span data-stu-id="d0421-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="d0421-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d0421-132">NOTES</span></span>

## <span data-ttu-id="d0421-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d0421-133">RELATED LINKS</span></span>

[<span data-ttu-id="d0421-134">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="d0421-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
