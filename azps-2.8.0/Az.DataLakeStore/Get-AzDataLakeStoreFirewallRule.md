---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 39450f979a4c79e453c66845b522aba91757f672
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752326"
---
# <span data-ttu-id="e7858-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e7858-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="e7858-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7858-102">SYNOPSIS</span></span>
<span data-ttu-id="e7858-103">Belirtilen veri Lake Store 'da belirtilen güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="e7858-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="e7858-104">Güvenlik duvarı kuralı belirtilmezse, hesabın tüm güvenlik duvarı kurallarını listeler.</span><span class="sxs-lookup"><span data-stu-id="e7858-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="e7858-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7858-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7858-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7858-106">DESCRIPTION</span></span>
<span data-ttu-id="e7858-107">Get-AzDataLakeStoreFirewallRule cmdlet 'i belirtilen veri Lake Store 'da belirtilen güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="e7858-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="e7858-108">Güvenlik duvarı kuralı belirtilmezse, hesabın tüm güvenlik duvarı kurallarını listeler.</span><span class="sxs-lookup"><span data-stu-id="e7858-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="e7858-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7858-109">EXAMPLES</span></span>

### <span data-ttu-id="e7858-110">Örnek 1: belirli bir güvenlik duvarı kuralını alma</span><span class="sxs-lookup"><span data-stu-id="e7858-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="e7858-111">"Benimfirewallrule" adlı güvenlik duvarı kuralını "ContosoADL" hesabından döndürür</span><span class="sxs-lookup"><span data-stu-id="e7858-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="e7858-112">Örnek 2: bir hesaptaki tüm güvenlik duvarı kurallarını listeleme</span><span class="sxs-lookup"><span data-stu-id="e7858-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="e7858-113">"ContosoADL" hesabındaki tüm güvenlik duvarı kurallarını döndürür</span><span class="sxs-lookup"><span data-stu-id="e7858-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="e7858-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7858-114">PARAMETERS</span></span>

### <span data-ttu-id="e7858-115">-Hesap</span><span class="sxs-lookup"><span data-stu-id="e7858-115">-Account</span></span>
<span data-ttu-id="e7858-116">Güvenlik duvarı kuralının alınacağı veri Lake Store hesabı.</span><span class="sxs-lookup"><span data-stu-id="e7858-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="e7858-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7858-117">-DefaultProfile</span></span>
<span data-ttu-id="e7858-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e7858-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7858-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7858-119">-Name</span></span>
<span data-ttu-id="e7858-120">Alınacak güvenlik duvarı kuralının adı</span><span class="sxs-lookup"><span data-stu-id="e7858-120">The name of the firewall rule to retrieve</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7858-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7858-121">-ResourceGroupName</span></span>
<span data-ttu-id="e7858-122">Belirtilen hesabın belirtilen güvenlik duvarı kuralını almak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e7858-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="e7858-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7858-123">CommonParameters</span></span>
<span data-ttu-id="e7858-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7858-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7858-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7858-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7858-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7858-126">INPUTS</span></span>

### <span data-ttu-id="e7858-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e7858-127">System.String</span></span>

## <span data-ttu-id="e7858-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7858-128">OUTPUTS</span></span>

### <span data-ttu-id="e7858-129">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e7858-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="e7858-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7858-130">NOTES</span></span>

## <span data-ttu-id="e7858-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7858-131">RELATED LINKS</span></span>
