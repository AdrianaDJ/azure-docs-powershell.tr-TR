---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 49674f372e477ee7050a6ccf7d833aaee59bac3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589178"
---
# <span data-ttu-id="90dac-101">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="90dac-101">Remove-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="90dac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90dac-102">SYNOPSIS</span></span>
<span data-ttu-id="90dac-103">Veri kaynağını siler.</span><span class="sxs-lookup"><span data-stu-id="90dac-103">Deletes a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90dac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90dac-104">SYNTAX</span></span>

### <span data-ttu-id="90dac-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="90dac-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90dac-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="90dac-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90dac-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="90dac-107">DESCRIPTION</span></span>
<span data-ttu-id="90dac-108">**Remove-Azurermoperationalınsightsdatasource** cmdlet 'i bir veri kaynağını siler.</span><span class="sxs-lookup"><span data-stu-id="90dac-108">The **Remove-AzureRmOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="90dac-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90dac-109">EXAMPLES</span></span>

## <span data-ttu-id="90dac-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90dac-110">PARAMETERS</span></span>

### <span data-ttu-id="90dac-111">-Force</span><span class="sxs-lookup"><span data-stu-id="90dac-111">-Force</span></span>
<span data-ttu-id="90dac-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="90dac-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90dac-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="90dac-113">-Name</span></span>
<span data-ttu-id="90dac-114">Silinecek veri kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90dac-114">Specifies the name of a data source to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90dac-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90dac-115">-ResourceGroupName</span></span>
<span data-ttu-id="90dac-116">Bilgisayarları içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90dac-116">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90dac-117">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="90dac-117">-Workspace</span></span>
<span data-ttu-id="90dac-118">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90dac-118">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90dac-119">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="90dac-119">-WorkspaceName</span></span>
<span data-ttu-id="90dac-120">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90dac-120">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90dac-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="90dac-121">-Confirm</span></span>
<span data-ttu-id="90dac-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="90dac-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90dac-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90dac-123">-WhatIf</span></span>
<span data-ttu-id="90dac-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="90dac-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90dac-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="90dac-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90dac-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90dac-126">-DefaultProfile</span></span>
<span data-ttu-id="90dac-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="90dac-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90dac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90dac-128">CommonParameters</span></span>
<span data-ttu-id="90dac-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90dac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90dac-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90dac-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90dac-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90dac-131">INPUTS</span></span>

### <span data-ttu-id="90dac-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="90dac-132">PSWorkspace</span></span>
<span data-ttu-id="90dac-133">Parametre ' çalışma alanı ', ardışık düzenin ' PSWorkspace ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="90dac-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="90dac-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90dac-134">OUTPUTS</span></span>

## <span data-ttu-id="90dac-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90dac-135">NOTES</span></span>
* <span data-ttu-id="90dac-136">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, işletim, Öngörüler</span><span class="sxs-lookup"><span data-stu-id="90dac-136">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="90dac-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90dac-137">RELATED LINKS</span></span>

[<span data-ttu-id="90dac-138">Get-Azurermoperationalınsightsdatasource</span><span class="sxs-lookup"><span data-stu-id="90dac-138">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="90dac-139">Set-Azurermoperationalınsightsdatasource</span><span class="sxs-lookup"><span data-stu-id="90dac-139">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


