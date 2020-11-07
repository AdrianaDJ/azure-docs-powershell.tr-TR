---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: bf57ffe0823ced37eaf58e9321c4330002c9be48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751573"
---
# <span data-ttu-id="c3c84-101">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c3c84-101">Get-AzIntegrationAccount</span></span>

## <span data-ttu-id="c3c84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3c84-102">SYNOPSIS</span></span>
<span data-ttu-id="c3c84-103">Tümleştirme hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="c3c84-103">Gets integration accounts.</span></span>

## <span data-ttu-id="c3c84-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3c84-104">SYNTAX</span></span>

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3c84-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3c84-105">DESCRIPTION</span></span>
<span data-ttu-id="c3c84-106">**Get-Azıntegrationaccount** cmdlet 'i bir kaynak grubundan tümleştirme hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="c3c84-106">The **Get-AzIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="c3c84-107">Tümleştirme hesap adını ve kaynak grubu adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="c3c84-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="c3c84-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="c3c84-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c3c84-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="c3c84-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c3c84-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="c3c84-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c3c84-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="c3c84-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c3c84-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3c84-112">EXAMPLES</span></span>

### <span data-ttu-id="c3c84-113">Örnek 1: ada göre tümleştirme hesabı alma</span><span class="sxs-lookup"><span data-stu-id="c3c84-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="c3c84-114">Bu komut, belirtilen kaynak grubundan IntegrationAccount31 adlı bir tümleştirme hesabı alır.</span><span class="sxs-lookup"><span data-stu-id="c3c84-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="c3c84-115">Örnek 2: kaynak grubunda tümleştirme hesapları alma</span><span class="sxs-lookup"><span data-stu-id="c3c84-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="c3c84-116">Bu komut, ResourceGroup11 adlı bir kaynak grubundan tümleştirme hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="c3c84-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="c3c84-117">Örnek 3: tüm tümleştirme hesaplarını alma</span><span class="sxs-lookup"><span data-stu-id="c3c84-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="c3c84-118">Bu komut, Azure aboneliğinizdeki tüm tümleştirme hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="c3c84-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="c3c84-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3c84-119">PARAMETERS</span></span>

### <span data-ttu-id="c3c84-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3c84-120">-DefaultProfile</span></span>
<span data-ttu-id="c3c84-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c3c84-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3c84-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="c3c84-122">-Name</span></span>
<span data-ttu-id="c3c84-123">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3c84-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="c3c84-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3c84-124">-ResourceGroupName</span></span>
<span data-ttu-id="c3c84-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3c84-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c3c84-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3c84-126">CommonParameters</span></span>
<span data-ttu-id="c3c84-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3c84-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3c84-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3c84-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3c84-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3c84-129">INPUTS</span></span>

### <span data-ttu-id="c3c84-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c3c84-130">System.String</span></span>

## <span data-ttu-id="c3c84-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3c84-131">OUTPUTS</span></span>

### <span data-ttu-id="c3c84-132">Microsoft. Azure. Management. Logic. modeller. ıntegrationhesabı</span><span class="sxs-lookup"><span data-stu-id="c3c84-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="c3c84-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3c84-133">NOTES</span></span>

## <span data-ttu-id="c3c84-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3c84-134">RELATED LINKS</span></span>

[<span data-ttu-id="c3c84-135">Get-Azıntegrationaccountcallbackurl</span><span class="sxs-lookup"><span data-stu-id="c3c84-135">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="c3c84-136">Yeni-azya hesabı</span><span class="sxs-lookup"><span data-stu-id="c3c84-136">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="c3c84-137">Remove-Azıntegrationaccount</span><span class="sxs-lookup"><span data-stu-id="c3c84-137">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="c3c84-138">Set-Azıntegrationaccount</span><span class="sxs-lookup"><span data-stu-id="c3c84-138">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


