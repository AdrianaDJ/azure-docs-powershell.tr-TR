---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
ms.openlocfilehash: 441681cd33fe7715fbbb6fb244848c287f14ebb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587903"
---
# <span data-ttu-id="bc3be-101">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="bc3be-101">Get-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="bc3be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc3be-102">SYNOPSIS</span></span>
<span data-ttu-id="bc3be-103">Tümleştirme hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="bc3be-103">Gets integration accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc3be-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc3be-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc3be-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc3be-105">DESCRIPTION</span></span>
<span data-ttu-id="bc3be-106">**Get-AzureRmIntegrationAccount** cmdlet 'i, bir kaynak grubundan tümleştirme hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="bc3be-106">The **Get-AzureRmIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="bc3be-107">Tümleştirme hesap adını ve kaynak grubu adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="bc3be-107">Specify an integration account name and resource group name.</span></span>

<span data-ttu-id="bc3be-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="bc3be-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="bc3be-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="bc3be-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="bc3be-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="bc3be-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bc3be-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="bc3be-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="bc3be-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc3be-112">EXAMPLES</span></span>

### <span data-ttu-id="bc3be-113">Örnek 1: ada göre tümleştirme hesabı alma</span><span class="sxs-lookup"><span data-stu-id="bc3be-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="bc3be-114">Bu komut, belirtilen kaynak grubundan IntegrationAccount31 adlı bir tümleştirme hesabı alır.</span><span class="sxs-lookup"><span data-stu-id="bc3be-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="bc3be-115">Örnek 2: kaynak grubunda tümleştirme hesapları alma</span><span class="sxs-lookup"><span data-stu-id="bc3be-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="bc3be-116">Bu komut, ResourceGroup11 adlı bir kaynak grubundan tümleştirme hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="bc3be-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="bc3be-117">Örnek 3: tüm tümleştirme hesaplarını alma</span><span class="sxs-lookup"><span data-stu-id="bc3be-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="bc3be-118">Bu komut, Azure aboneliğinizdeki tüm tümleştirme hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="bc3be-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="bc3be-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc3be-119">PARAMETERS</span></span>

### <span data-ttu-id="bc3be-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="bc3be-120">-Name</span></span>
<span data-ttu-id="bc3be-121">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc3be-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc3be-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc3be-122">-ResourceGroupName</span></span>
<span data-ttu-id="bc3be-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc3be-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc3be-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc3be-124">-DefaultProfile</span></span>
<span data-ttu-id="bc3be-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc3be-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc3be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc3be-126">CommonParameters</span></span>
<span data-ttu-id="bc3be-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc3be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc3be-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc3be-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc3be-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc3be-129">INPUTS</span></span>

## <span data-ttu-id="bc3be-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc3be-130">OUTPUTS</span></span>

### <span data-ttu-id="bc3be-131">Microsoft. Azure. Management. Logic. modeller. ıntegrationhesabı</span><span class="sxs-lookup"><span data-stu-id="bc3be-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="bc3be-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc3be-132">NOTES</span></span>

## <span data-ttu-id="bc3be-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc3be-133">RELATED LINKS</span></span>

[<span data-ttu-id="bc3be-134">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="bc3be-134">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="bc3be-135">Yeni-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="bc3be-135">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="bc3be-136">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="bc3be-136">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="bc3be-137">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="bc3be-137">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


