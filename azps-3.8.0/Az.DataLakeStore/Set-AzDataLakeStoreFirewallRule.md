---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5c807c3d134768c7682b2216178eabd5a0771701
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94105035"
---
# <span data-ttu-id="5fee2-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5fee2-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="5fee2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fee2-102">SYNOPSIS</span></span>
<span data-ttu-id="5fee2-103">Belirtilen veri Lake Store 'da belirtilen güvenlik duvarı kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5fee2-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="5fee2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5fee2-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fee2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5fee2-105">DESCRIPTION</span></span>
<span data-ttu-id="5fee2-106">**Set-AzDataLakeStoreFirewallRule** cmdlet 'ı belirtilen veri</span><span class="sxs-lookup"><span data-stu-id="5fee2-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="5fee2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5fee2-107">EXAMPLES</span></span>

### <span data-ttu-id="5fee2-108">Örnek 1: güvenlik duvarı kuralı için başlangıç ve bitiş IP aralığını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5fee2-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="5fee2-109">"ContosoADL" hesabındaki "MyFirewallRule" güvenlik duvarı</span><span class="sxs-lookup"><span data-stu-id="5fee2-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="5fee2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5fee2-110">PARAMETERS</span></span>

### <span data-ttu-id="5fee2-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="5fee2-111">-Account</span></span>
<span data-ttu-id="5fee2-112">Güvenlik duvarı kuralını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5fee2-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="5fee2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fee2-113">-DefaultProfile</span></span>
<span data-ttu-id="5fee2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5fee2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fee2-115">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="5fee2-115">-EndIpAddress</span></span>
<span data-ttu-id="5fee2-116">Güvenlik duvarı kuralı için geçerli IP aralığının sonu</span><span class="sxs-lookup"><span data-stu-id="5fee2-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fee2-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="5fee2-117">-Name</span></span>
<span data-ttu-id="5fee2-118">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="5fee2-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="5fee2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fee2-119">-ResourceGroupName</span></span>
<span data-ttu-id="5fee2-120">Güvenlik duvarı kuralını güncelleştirme hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fee2-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fee2-121">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="5fee2-121">-StartIpAddress</span></span>
<span data-ttu-id="5fee2-122">Güvenlik duvarı kuralı için geçerli IP aralığının başlangıcı</span><span class="sxs-lookup"><span data-stu-id="5fee2-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="5fee2-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="5fee2-123">-Confirm</span></span>
<span data-ttu-id="5fee2-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5fee2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fee2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fee2-125">-WhatIf</span></span>
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

### <span data-ttu-id="5fee2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fee2-126">CommonParameters</span></span>
<span data-ttu-id="5fee2-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5fee2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fee2-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fee2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fee2-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5fee2-129">INPUTS</span></span>

### <span data-ttu-id="5fee2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5fee2-130">System.String</span></span>

## <span data-ttu-id="5fee2-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5fee2-131">OUTPUTS</span></span>

### <span data-ttu-id="5fee2-132">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5fee2-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="5fee2-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5fee2-133">NOTES</span></span>

## <span data-ttu-id="5fee2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5fee2-134">RELATED LINKS</span></span>
