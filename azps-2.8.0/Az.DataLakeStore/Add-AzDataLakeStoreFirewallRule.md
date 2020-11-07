---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 9fa890ee6102f4751b62325b3cc3669d337cb6c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752353"
---
# <span data-ttu-id="0357f-101">Add-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0357f-101">Add-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="0357f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0357f-102">SYNOPSIS</span></span>
<span data-ttu-id="0357f-103">Belirtilen Data Lake Store hesabına bir güvenlik duvarı kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="0357f-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="0357f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0357f-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0357f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0357f-105">DESCRIPTION</span></span>
<span data-ttu-id="0357f-106">**Add-AzDataLakeStoreFirewallRule** cmdlet 'ı belirtilen Data Lake Store hesabına bir güvenlik duvarı kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="0357f-106">The **Add-AzDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="0357f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0357f-107">EXAMPLES</span></span>

### <span data-ttu-id="0357f-108">Örnek 1: veri Lake Store hesabına yeni bir güvenlik duvarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="0357f-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="0357f-109">Bu, "ContosoADL" hesabında "ContosoADL" adlı, 127.0.0.1-127.0.0.2 adlı yeni bir güvenlik duvarı kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="0357f-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="0357f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0357f-110">PARAMETERS</span></span>

### <span data-ttu-id="0357f-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="0357f-111">-Account</span></span>
<span data-ttu-id="0357f-112">Güvenlik duvarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="0357f-112">The Data Lake Store account to add the firewall rule to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0357f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0357f-113">-DefaultProfile</span></span>
<span data-ttu-id="0357f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0357f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0357f-115">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="0357f-115">-EndIpAddress</span></span>
<span data-ttu-id="0357f-116">Güvenlik duvarı kuralı için geçerli IP aralığının sonu</span><span class="sxs-lookup"><span data-stu-id="0357f-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="0357f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="0357f-117">-Name</span></span>
<span data-ttu-id="0357f-118">Eklenecek güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="0357f-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="0357f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0357f-119">-ResourceGroupName</span></span>
<span data-ttu-id="0357f-120">Güvenlik duvarı kuralının ekleneceği hesabın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0357f-120">Name of resource group under which the account to add the firewall rule is.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0357f-121">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="0357f-121">-StartIpAddress</span></span>
<span data-ttu-id="0357f-122">Güvenlik duvarı kuralı için geçerli IP aralığının başlangıcı</span><span class="sxs-lookup"><span data-stu-id="0357f-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0357f-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="0357f-123">-Confirm</span></span>
<span data-ttu-id="0357f-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0357f-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0357f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0357f-125">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0357f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0357f-126">CommonParameters</span></span>
<span data-ttu-id="0357f-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0357f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0357f-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0357f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0357f-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0357f-129">INPUTS</span></span>

### <span data-ttu-id="0357f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0357f-130">System.String</span></span>

## <span data-ttu-id="0357f-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0357f-131">OUTPUTS</span></span>

### <span data-ttu-id="0357f-132">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0357f-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="0357f-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0357f-133">NOTES</span></span>

## <span data-ttu-id="0357f-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0357f-134">RELATED LINKS</span></span>
