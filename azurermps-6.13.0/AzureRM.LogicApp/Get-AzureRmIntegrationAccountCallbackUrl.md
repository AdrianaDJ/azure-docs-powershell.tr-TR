---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 1a279eecfad19fc35bae7c9f1b3bf828a07913e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594013"
---
# <span data-ttu-id="4bf09-101">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="4bf09-101">Get-AzureRmIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="4bf09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bf09-102">SYNOPSIS</span></span>
<span data-ttu-id="4bf09-103">Tümleştirme hesabı geri çağırma URL 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="4bf09-103">Gets an integration account callback URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bf09-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4bf09-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bf09-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bf09-105">DESCRIPTION</span></span>
<span data-ttu-id="4bf09-106">**Get-AzureRmIntegrationAccountCallbackUrl** cmdlet 'i bir kaynak grubundan tümleştirme hesabı geri araması URL 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="4bf09-106">The **Get-AzureRmIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="4bf09-107">Bu cmdlet, tümleştirme hesabı geri çağırma URL 'sini temsil eden bir **Callbackurl** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="4bf09-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="4bf09-108">Tümleştirme hesap adını ve kaynak grup adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="4bf09-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="4bf09-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="4bf09-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4bf09-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="4bf09-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4bf09-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="4bf09-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4bf09-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="4bf09-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4bf09-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4bf09-113">EXAMPLES</span></span>

### <span data-ttu-id="4bf09-114">Örnek 1: Tümleştirme hesabı geri çağırma URL 'SI alma</span><span class="sxs-lookup"><span data-stu-id="4bf09-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="4bf09-115">Bu komut, tümleştirme hesabı geri çağırma URL 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="4bf09-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="4bf09-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4bf09-116">PARAMETERS</span></span>

### <span data-ttu-id="4bf09-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bf09-117">-DefaultProfile</span></span>
<span data-ttu-id="4bf09-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4bf09-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4bf09-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="4bf09-119">-Name</span></span>
<span data-ttu-id="4bf09-120">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bf09-120">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="4bf09-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="4bf09-121">-NotAfter</span></span>
<span data-ttu-id="4bf09-122">Geri arama URL 'sinin bitiş tarihini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bf09-122">Specifies the expiry date for the callback URL.</span></span>

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

### <span data-ttu-id="4bf09-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bf09-123">-ResourceGroupName</span></span>
<span data-ttu-id="4bf09-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bf09-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4bf09-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bf09-125">CommonParameters</span></span>
<span data-ttu-id="4bf09-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4bf09-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bf09-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bf09-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bf09-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4bf09-128">INPUTS</span></span>

### <span data-ttu-id="4bf09-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4bf09-129">System.String</span></span>

## <span data-ttu-id="4bf09-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4bf09-130">OUTPUTS</span></span>

### <span data-ttu-id="4bf09-131">Microsoft. Azure. Management. Logic. modeller. CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="4bf09-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="4bf09-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4bf09-132">NOTES</span></span>

## <span data-ttu-id="4bf09-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4bf09-133">RELATED LINKS</span></span>

[<span data-ttu-id="4bf09-134">Get-AzureRmLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="4bf09-134">Get-AzureRmLogicAppTriggerCallbackUrl</span></span>](./Get-AzureRmLogicAppTriggerCallbackUrl.md)


