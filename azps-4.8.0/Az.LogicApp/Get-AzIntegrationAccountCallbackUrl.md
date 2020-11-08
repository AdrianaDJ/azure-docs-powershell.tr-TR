---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 91a61935552258e5ca52ded6e05729deecaf5665
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267314"
---
# <span data-ttu-id="6828f-101">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="6828f-101">Get-AzIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="6828f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6828f-102">SYNOPSIS</span></span>
<span data-ttu-id="6828f-103">Tümleştirme hesabı geri çağırma URL 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="6828f-103">Gets an integration account callback URL.</span></span>

## <span data-ttu-id="6828f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6828f-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6828f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6828f-105">DESCRIPTION</span></span>
<span data-ttu-id="6828f-106">**Get-Azıntegrationaccountcallbackurl** cmdlet 'i, bir kaynak grubundan tümleştirme hesabı geri araması URL 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="6828f-106">The **Get-AzIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="6828f-107">Bu cmdlet, tümleştirme hesabı geri çağırma URL 'sini temsil eden bir **Callbackurl** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="6828f-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="6828f-108">Tümleştirme hesap adını ve kaynak grup adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="6828f-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="6828f-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="6828f-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6828f-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="6828f-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6828f-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="6828f-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6828f-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="6828f-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6828f-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6828f-113">EXAMPLES</span></span>

### <span data-ttu-id="6828f-114">Örnek 1: Tümleştirme hesabı geri çağırma URL 'SI alma</span><span class="sxs-lookup"><span data-stu-id="6828f-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="6828f-115">Bu komut, tümleştirme hesabı geri çağırma URL 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="6828f-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="6828f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6828f-116">PARAMETERS</span></span>

### <span data-ttu-id="6828f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6828f-117">-DefaultProfile</span></span>
<span data-ttu-id="6828f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6828f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6828f-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="6828f-119">-Name</span></span>
<span data-ttu-id="6828f-120">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6828f-120">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6828f-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="6828f-121">-NotAfter</span></span>
<span data-ttu-id="6828f-122">Geri arama URL 'sinin bitiş tarihini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6828f-122">Specifies the expiry date for the callback URL.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6828f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6828f-123">-ResourceGroupName</span></span>
<span data-ttu-id="6828f-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6828f-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6828f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6828f-125">CommonParameters</span></span>
<span data-ttu-id="6828f-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6828f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6828f-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6828f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6828f-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6828f-128">INPUTS</span></span>

### <span data-ttu-id="6828f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6828f-129">System.String</span></span>

## <span data-ttu-id="6828f-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6828f-130">OUTPUTS</span></span>

### <span data-ttu-id="6828f-131">Microsoft. Azure. Management. Logic. modeller. CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="6828f-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="6828f-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6828f-132">NOTES</span></span>

## <span data-ttu-id="6828f-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6828f-133">RELATED LINKS</span></span>

[<span data-ttu-id="6828f-134">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="6828f-134">Get-AzLogicAppTriggerCallbackUrl</span></span>](./Get-AzLogicAppTriggerCallbackUrl.md)


